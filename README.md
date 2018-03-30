# Sublime Text Configuration

This repository contains configuration of Sublime Text. I've
committed it to git, so that I can use it across my devices and
to have it in case I loose it, as I have lost it before and it
took a while before I was able to set everything the way it was.

This repository is supposed to be in:

```
/Users/lucian/Library/Application Support/Sublime Text 3/Packages/User
```

Use these settings without overriding your entire User folder:

```shell
cd "/Users/lucian/Library/Application Support/Sublime Text 3/Packages/"
git clone git@github.com:dlucian/sublime-config.git
cd User
ln -s ../sublime-config/Preferences.sublime-settings
ln -s ../sublime-config/php-unittest.sublime-snippet
# Start Sublime Text & Enjoy
```

This way you can only use whatever settings, files or snippets you want,
without loosing everything in your `User` folder. 

## Set MySQL Mode to be less strict

```shell
nano /usr/local/etc/my.cnf
```

Add this to the end of file, under the `[mysqld]` line:

```ini
sql_mode = "STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION"
```

Restart MySQL

```shell
brew services restart mysql
```

## Set per-project settings in Sublime

```
{
	"folders":
	[
		{
			"path": "."
		}
	],
	"settings":
	{
        "trim_trailing_white_space_on_save": true
	}
}
```

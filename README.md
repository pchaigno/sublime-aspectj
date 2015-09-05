# Syntax highlighting for AspectJ

This package provides syntax highlighting for Sublime Text 2 and 3.
It is also used to highlight AspectJ code on GitHub (in files, Gists and Markdown documents).

## Installation

### Package Control

I recommend using [Package Control](https://packagecontrol.io/), the Sublime Text package manager to install this package. It is much more convenient.

### Manual installation

To install this package manually, please do:

```
cd /tmp
wget -O sublime-aspectj.tar.gz http://github.com/pchaigno/sublime-aspectj/tarball/master
tar -xzvf sublime-aspectj.tar.gz
mv pchaigno-sublime-aspectj-*/*.tmLanguage ~/.config/sublime-text-2/Packages/User/
```

## GitHub preview

```aspectj
public aspect CacheAspect {

	public pointcut cache(Cachable c): execution(@Cachable * * (..)) && @annotation(c);
	
	Object around(Cachable cachable): cache(cachable) {
		return proceed(cachable);
	}
}
```


## License

This package is under [MIT license](LICENSE).

The Java syntax is based on https://github.com/textmate/java.tmbundle.

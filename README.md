# Syntax highlighting for AspectJ

This package provides syntax highlighting for Sublime Text 2 and 3.
It is also used to highlight AspectJ code on GitHub (in files, Gists and Markdown documents).

## Installation

To install this package, please do:

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

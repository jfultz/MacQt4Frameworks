## Mac Qt4 frameworks

**Problem:**

The frameworks added to apps by `macdeployqt` cannot be signed by `codesign`


**Symptom:**

````
codesign -s identity --deep --force Foo.app
Foo.app: replacing existing signature
Foo.app: bundle format unrecognized, invalid, or unsuitable
In subcomponent: Foo.app/Contents/Frameworks/QtCore.framework
````

**Solution:**

Bah...I can never remember how to do this.  Some guy's python script which blah-blah-blah and which didn't work and needs modification blah-blah-blah.

**Other solution:**

Copy Frameworks/ into your *.app file.  Then `codesign -s identity --deep --force` your entire app bundle.  This is Qt 4.8.6, as distributed by HomeBrew, with default options.

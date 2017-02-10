### Installing sublime text `Package Control`

- To install sublime plug-ins, first we have to install `package control`. Follow the below instructions to install package control
    + The instructions are taken from [https://packagecontrol.io/installation](https://packagecontrol.io/installation)
    + Open sublime text application, then access the console using  ``Ctrl +` `` (or) go to the `view -> show console`
    + Then paste the appropriate Python code for your version of Sublime Text into the console.

```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

- Then restart the sublime text application

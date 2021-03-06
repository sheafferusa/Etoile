Etoile HACKING
==============

Here is a short summary of the rules to follow when you contribute to Etoile.

1) You must read and apply [Coding Style Guidelines](http://etoileos.com/dev/codingstyle/).

Any new modules to be committed must comply with them, older modules should be
updated gradually (take care of this when you modify the code in an important
manner).

There are no coding guidelines for languages other than Objective-C, so you are
almost free to do whatever you want in such case :-) well, until someone extend
Coding Guidelines to include your language.


2) You must build the whole repository (make in `trunk/Etoile`) regularly and
specially on:
- each group of related commits
- any repository structural changes (module added, renamed, moved etc.)
- any build support changes

If you discover the repository build is broken on your platform, take time to
check if you haven't broken it in some way with your last commits. In any
case, if you are unable to fix the problem, send a mail to etoile-dev list
outlining the build issue you encounter (don't forget to mention your platform
and setup).

3) You must usually conform to usual project layout for the module you
maintain.

An important point is to always include etoile.make in your main
GNUmakefile to ensure other modules can access it at build time (for example
a bundle module can link your framework module).
You can find templates for frameworks, applications etc. in [Developer/Templates](http://svn.gna.org/viewcvs/etoile/trunk/Etoile/Developer/Templates/)

4) All defaults exported in `NSGlobalDomain` or publicly documented must use 'ET'
prefix.

This choice makes easier to quickly distinguish the defaults which have been set
by Etoile. All other defaults use no prefix or their own prefix like 'NS' and 'GS'
in GNUstep case.

---

Here is a short summary of various development aids you could be interested in:

- Examples of typical framework use (in [Developer/Examples](http://svn.gna.org/viewcvs/etoile/trunk/Etoile/Developer/Examples/))

- [Framework API documentation](http://etoileos.com/dev/docs/frameworks/)

- [Participate](http://etoileos.com/dev/) section of the web site (Coding style, Subversion help)

- [etoile-dev](https://mail.gna.org/listinfo/etoile-dev/) list by subscribing or reading the archive

- [Etoile News](http://etoileos.com/news/) development blog (includes tutorials and technical discussions)

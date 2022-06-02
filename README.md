# Plagiat NON

This is a mostly focused on non-mixer with hacks and quality of life improvements for the plagiat brothers. Other non-apps may break.


# NON

## Non-things build instructions

This repository contains all of the non-* software.

### Getting NTK

If you just cloned the non repository or just executed git pull, then
you should also run

```
git submodule update --init
```

to pull down the latest NTK code required by Non. Git does *not* do
this automatically.

### Building NTK

If you don't have NTK installed system-wide (which isn't very likely
yet) you *MUST* begin the build process by typing:

```
cd lib/ntk
./waf configure
./waf
```

Once NTK has been built you must install it system-wide before
attempting to build the non-* programs.

To install NTK type:

```
su -c './waf install'
```

### Build all projects

Typing:

```
./waf configure
./waf
 su -c './waf install'
```
    
from the base of the checkout of the Non git repository will build and
install all of the non-* programs together.

### Build a single project

Typing:

```
./waf configure --project=[timline|sequencer|mixer|session-manager]
./waf
su -c './waf install'
```


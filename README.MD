[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/scoop-software/openjfx-win/blob/master/LICENSE)
[![Build status](https://ci.appveyor.com/api/projects/status/da1javueht7fml8p?svg=true)](https://ci.appveyor.com/project/siordache/openjfx-win)

## OpenJFX 8 binaries for Windows ##

This project uses [AppVeyor](https://www.appveyor.com/) to create OpenJFX 8 binaries and make them available on the [releases](https://github.com/scoop-software/openjfx-win/releases) page.
It also puts up an OpenJDK distribution that includes OpenJFX.

You can customize the AppVeyor build by editing the variables declared in the `environment` section of
[.appveyor.yml](https://github.com/scoop-software/openjfx-win/blob/master/.appveyor.yml):
- `OPENJFX_TAG`: the OpenJFX version to be built. It must correspond to an existing [Mercurial tag](https://hg.openjdk.java.net/openjfx/8u-dev/rt/tags).
- `OPEN_JDK_URL`: the URL of the desired OpenJDK version. It must be in sync with
the value of `OPEN_JDK_DIR`.
- `OPEN_JDK_DIR`: the root directory of the files in the archive located at `OPEN_JDK_URL`.

If you fork this project, you need to create a [personal access token](https://github.com/settings/tokens) with `repo` or `public_repo` scope,
[encrypt](https://ci.appveyor.com/tools/encrypt) its value, and
include the resulting string in `.appveyor.yml`, as the secure value of the `auth_token` deployment variable.

# Build Cheat Engine

CE has an [official appveyor.yml](https://github.com/cheat-engine/cheat-engine/blob/master/appveyor.yml), but it's not public for downloading artifacts.

This repo builds CE via GitHub Actions and release binaries to artifacts.

Big thanks to scripts from PhantomGamers/cheat-engine

## Pitfalls

* CE doesn't support 2.2 yet. You must use 2.0.10, i.e. the required version in README, otherwise it will reports `Error: (5000) Identifier not found "TSynEditorOptions"`
* In CI with `lazarus-2.2.0-fpc-3.2.2-win64.exe /verysilent`, it will report `invalid Lazarus directory "": directory lcl not found`

## Other builds

* https://github.com/PhantomGamers/cheat-engine
* https://github.com/PandaSt0rm/cheat-engine-builds
* https://github.com/SakuradeMiku/cheat-engine
* https://github.com/mrdellis/cheat-engine
* https://github.com/kratos284/cheat-engine Failed
* https://github.com/instantsc/cheat-engine Failed

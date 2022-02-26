# Build Cheat Engine

If you try to download CE from https://cheatengine.org/ or even it's GitHub Releases, you will actually get a downloader, which will ~~silently~~ install some malwares such as *RAV Antivirus*. I just found that the installer actually asked you whether to *Accept* installing RAV and you can click *Decline*. But I think it's not friendly to non-English users because they have difficulty reading carefully.

CE has an [official appveyor.yml](https://github.com/cheat-engine/cheat-engine/blob/master/appveyor.yml), but it's not open for public to download. I also tried using Charles to get the installer from https://d2oq4dwfbh6gxl.cloudfront.net/f/CheatEngine/DOTPS-556/CheatEngine74.exe, but it refuses to install and says *Please execute this from the correct installer*.

This repo builds CE via GitHub Actions and release binaries to artifacts.

It only builds the Main application. Components such as tutorial and DBVM are not included. It builds x86_64 version and requires your CPU to support AVX2. These can be easily changed via the commented out command in yml.

Big thanks to scripts from PhantomGamers/cheat-engine.

## Pitfalls

* CE doesn't support 2.2 yet. You must use 2.0.10, i.e. the required version in README, otherwise it will report `Error: (5000) Identifier not found "TSynEditorOptions"`
* When use `lazarus-2.2.0-fpc-3.2.2-win64.exe /verysilent` in CI, it will report `invalid Lazarus directory "": directory lcl not found`. So I changed to use gcarreno/setup-lazarus

## Other builds

* https://github.com/PhantomGamers/cheat-engine
* https://github.com/PandaSt0rm/cheat-engine-builds
* https://github.com/SakuradeMiku/cheat-engine
* https://github.com/mrdellis/cheat-engine
* https://github.com/kratos284/cheat-engine Failed
* https://github.com/instantsc/cheat-engine Failed

## TODO

* 集成 https://cheatengine.org/download/zh_CN_All.7z

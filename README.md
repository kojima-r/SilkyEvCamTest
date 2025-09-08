# SilkyEvCamTest


現在フリーで使えるのは Metavision SDK 4.6まで（5.xはProphesee製品であれば登録できるらしいが、SilkyEvCamは対象外）
https://www.prophesee.ai/metavision-intelligence-sdk-download/

- Metavision SDK version 4.6.2
- Ubuntu 22.04/amd64(x86)までしか対応していないので注意

一応、OpenEB 5.0 のopen moduleに限ればできるらしいが未調査 https://docs.prophesee.ai/stable/installation/index.html

基本的に以下の手順にしたがってインストールしたあと
https://docs.prophesee.ai/4.6.2/installation/linux.html#chapter-installation-linux
インストールがうまく行っていれば`metavision_studio`コマンドが使えて起動する（この時点ではカメラをつないでも認識しない）

以下の「Plug-in & Firmware for METAVISION® SDK V4.6.2」のプラグインをインストール
https://centuryarks.com/en/download/
展開して、コマンドを実行するだけ
```
./CA_Silky_installer.sh
```
インストール後に再起動する必要があったが、
`metavision_studio`コマンドでmetavision_studioを起動したあとにカメラを認識するようになっていれば成功

pythonを入れていればpython経由での利用が可能
`src/`

Ubuntu22.04にapt経由で入れていれば以下にpythonのサンプルが保存されいてる
```
/usr/share/metavision/sdk/core/python_samples/
```

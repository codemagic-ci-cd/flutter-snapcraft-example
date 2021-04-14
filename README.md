# flutter_codemagic_example

# flutter_codemagic_example

## Create snap

    snapcraft snap --output flutter-snapcraft-example.snap

## Clean

    snapcraft clean flutter-snapcraft-example -s pull

## Install (without codesigning)

    sudo snap install flutter-snapcraft-example.snap --dangerous

## Login

    snapcraft export-login snapcraft-login-credentials

Will create a file `snapcraft-login-credentials`. To login in CI/CD environment use

    snapcraft login --with snapcraft-login-credentials

## Publish

    snapcraft register flutter-snapcraft-example # if not already
    snapcraft upload flutter-snapcraft-example.snap
    snapcraft release flutter-snapcraft-example revision-number channel
    
 
Channels: `stable`, `candidate`, `beta`, and `edge`

## Install from snapcraft

    sudo snap install flutter-snapcraft-example

## Uninstall

    sudo snap remove flutter-snapcraft-example

# Install snapcraft on macOS

    brew install --cask multipass
    brew install snapcraft

Doesn't provide ability to download from snapcraft

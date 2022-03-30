# Install on macOS

macOS에서 Vapor를 사용하려면, Swift 5.2 혹은 그 이상이 필요합니다. Swift와 다른 모든 의존성들은 Xcode에 포함되어 있습니다.

## Install Xcode

[Xcode 11.4 혹은 그 이상](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)을 Mac App Store에서 설치해주세요.

![Xcode in Mac App Store](../images/xcode-mac-app-store.png)

Xcode를 다운로드 한 후, 설치를 완료하기 위해서 반드시 실행해야 합니다. 이 작업은 시간이 소요될 수 있습니다.

설치가 성공했는지 확인하기 위해서 터미널을 열고 Swift 버전을 확인합니다.

```sh
swift --version
```

Swift의 버전 정보가 출력된 것을 볼 수 있을 것입니다.

```sh
Apple Swift version 5.2 (swiftlang-1100.0.270.13 clang-1100.0.33.7)
Target: x86_64-apple-darwin19.0.0
```

Vapor 4는 Swift 5.2 혹은 그 이상이 필요합니다.

## Install Toolbox

이제 Swift가 설치되었으니, [Vapor Toolbox](https://github.com/vapor/toolbox)를 설치합니다. 이 CLI tool은 Vapor를 사용하기 위해 필수적이지는 않지만 new project creator와 같은 유용한 유틸리티가 포함되어 있습니다.

Toolbox는 Homebrew에 배포되어 있습니다. Homebrew가 없다면, <a href="https://brew.sh" target="_blank">brew.sh</a>를 방문하여 설치 지침을 알아보세요.

```sh
brew install vapor
```

설치 성공 확인을 위해 도움말을 출력해보세요.

```sh
vapor --help
```

사용가능한 커맨드들의 리스트를 볼 수 있을겁니다.

## Next

이제 Swift와 Vapor Toolbox를 설치했습니다. [Getting Started &rarr; Hello, world](../hello-world.md)에서 첫 앱을 만드세요.

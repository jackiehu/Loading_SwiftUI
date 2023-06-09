# Loading_SwiftUI

[![SPM](https://img.shields.io/badge/SPM-supported-DE5C43.svg?style=flat)](https://swift.org/package-manager/)
![Xcode 14.0+](https://img.shields.io/badge/Xcode-14.0%2B-blue.svg)
![iOS 14.0+](https://img.shields.io/badge/iOS-14.0%2B-blue.svg)
![Swift 5.0+](https://img.shields.io/badge/Swift-5.0%2B-orange.svg)
![SwiftUI 3.0+](https://img.shields.io/badge/SwiftUI-3.0%2B-orange.svg)

|                        |                         |                         |                         |                          |
| ---------------------- | ----------------------- | ----------------------- | ----------------------- | ------------------------ |
| ![](Image/loading.png) | ![](Image/loading2.png) | ![](Image/loading3.png) | ![](Image/progress.png) | ![](Image/progress2.png) |
| ![](Image/succ.png)    | ![](Image/succ2.png)    | ![](Image/fail.png)     | ![](Image/fail2.png)    |                          |



Loading_SwiftUI is a loading pop-up tool developed based on SwiftUI. It has several built-in styles, including Loading, Progress, Success, and Fail. Style reference [ProgressHUD](https://github.com/relatedcode/ProgressHUD).



```swift
loading.showLoading()
loading.showProgress()
loading.showSuccess()
loading.showFail()

loading.dismiss()
```

You can also customize your own Loading style, without any intrusion, no inheritance, completely native, just need to extend the method of the controller

```swift
extension LoadingManager {
    //展示自定义View//自己可以重写替换
   func showCustom(){
        show {
            CustomView()
        }
    }
}
```

## Usage

Create a controller on the page that needs to pop up Toast

```swift
    @EnvironmentObject private var loading: LoadingManager
    //OR
    @StateObject var loading = LoadingManager()
```

Add a controller to the page

```
.addLoading(loading)
```

Control the position where Toast pops up, and then call the show method

```
loading.showLoading()
```

controller

```swift
    //HUD提示
    @Published public var text: String?
    //HUD提示字体颜色
    @Published public var textColor = Color.black
    //HUD提示字体颜色
    @Published public var textFont: Font = .system(size: 15, weight: .medium)
    //HUD Loading颜色
    @Published public var accentColor = Color.blue
    ///进度条进度 0--1
    @Published public var progress: CGFloat = 0
```




## Install

### Cocoapods

1. Add `pod 'Loading_SwiftUI'` to Podfile

2. Execute `pod install or pod update`

3. Import `import Loading_SwiftUI`

### Swift Package Manager

Starting from Xcode 11, the Swift Package Manager is integrated, which is very convenient to use. Loading_SwiftUI also supports integration via the Swift Package Manager.

Select `File > Swift Packages > Add Pacakage Dependency` in Xcode's menu bar, and enter in the search bar

`https://github.com/jackiehu/Loading_SwiftUI`, you can complete the integration

### Manual integration

Loading_SwiftUI also supports manual integration, just drag the SwiftMediator folder in the Sources folder into the project that needs to be integrated


## Author

jackiehu, 814030966@qq.com

## More brick tools to speed up APP development

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftMediator&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftMediator)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftBrick&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftBrick)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftShow&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftShow)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftLog&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftLog)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftyForm&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftyForm)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftEmptyData&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftEmptyData)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftPageView&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftPageView)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=JHTabBarController&theme=radical&locale=cn)](https://github.com/jackiehu/JHTabBarController)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftMesh&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftMesh)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftNotification&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftNotification)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftNetSwitch&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftNetSwitch)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftButton&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftButton)

[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=jackiehu&repo=SwiftDatePicker&theme=radical&locale=cn)](https://github.com/jackiehu/SwiftDatePicker)


## 许可

Loading_SwiftUI is available under the MIT license. See the LICENSE file for more info.

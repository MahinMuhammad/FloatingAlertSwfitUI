# FloatingAlert-SwiftUI

Floating Alert is a custom package for swiftUI. It enables simple and easy to implement temporary popup Alerts that autometically fade away after few moments.

If you like the project, please do not forget to star ★ this repository and follow me on GitHub.

## Preview 

<table style="border:none">
  <tr>
    <td><img src="/Graphics/FloatingAlert.gif" width="200" height="400"></td>
  </tr>
</table>

## Requirements

* iOS 13.0+
* Xcode 11.2+
* Swift 5.0
* SwiftUI framework

##Features

* Customizable floating alert view with image and message parameters
* Customizable time parameter to keep the alert on display for a perticular moment
* Parameters for a cusomized look of the alert view

## Installation

### **Swift Package Manager**

You can add FloatingAlert-SwiftUI as a dependency in your Swift Package Manager-enabled project. 
Follow these steps to integrate the package into your project:

1. In Xcode, go to "File" -> "Add Packages...".
2. Enter the URL of this repository: https://github.com/MahinMuhammad/FloatingAlertSwfitUI
3. Choose the desired version rule.
4. Chosse the target where you want to add the package.
5. Click "Add Package".
6. Wait till Xcode varify and fetch it for you.
7. Click "Add Package".

## Usage

To use FloatingAlert-SwiftUI in your SwiftUI project, follow these steps:

1. Import the CheckBoxSwiftUI module:
```swift
import FloatingAlert
```

2. Create a @State property to hold the FloatingAlert view state:
```swift
@State var showFloatingAlert = false
```

3. Use the 'CheckBox' view in your SwiftUI ZStack view hierarchy:
```swift
ZStack{
    //other views
    if viewModel.showCopiedToClipboardAlert {
        FloatingAlertView(showingNotice: $showFloatingAlert, image: Image(systemName: "doc.on.clipboard"), message: "Copied to Clipboard")
    }
}
```

4. Add this line when you want to show the alert
```swift
showFloatingAlert = true
```

5. Customize the FloatingAlert appearance by providing optional parameters:
```swift
ZStack{
    //other views
    if viewModel.showCopiedToClipboardAlert {
        FloatingAlertView(showingNotice: $viewModel.showCopiedToClipboardAlert, image: Image(systemName: "doc.on.clipboard"), activeTime: 1.2, message: "Copied to Clipboard", opacity: 0.90, cornerRadious: 35, imageSize: 48)
    }
}
```

## Integration into a complete but simple code:

```swift
import SwiftUI
import FloatingAlert

struct ContentView: View {
@State var showFloatingAlert = false

    var body: some View {
        ZStack{
            VStack{
                Button("Copy") {
                    showFloatingAlert = true
                }
            }
            .padding()
            
            if viewModel.showCopiedToClipboardAlert {
                FloatingAlertView(showingNotice: $showFloatingAlert, image: Image(systemName: "doc.on.clipboard"), message: "Copied to Clipboard")
            }
        }
    }
}

```


## Author

Md. Mahinur Rahman, <br>
iOS Developer <br>
rahmanmahin@icloud.com

## Find Me on:

[FaceBook](https://web.facebook.com/mahin5muhammad)
[Instagram](https://www.instagram.com/mahin5muhammad/)
[LinkedIn](https://www.linkedin.com/in/rahmanmahin/)
[Twitter](https://twitter.com/ImMahin)
[Website](https://mahinmuhammad.github.io/view/home.html)
[Discord](http://discordapp.com/users/Ghost_Friday#2625)

## Contributing

Contributions to FloatingAlert-SwiftUI are welcome! If you encounter any issues or have ideas for improvements, please feel free to open an issue or submit a pull request.

## Feedback

Please feel free to open any [issue](https://github.com/MahinMuhammad/FloatingAlertSwfitUI/issues)

## License

FloatingAlert-SwiftUI is available under the MIT License. See the LICENSE file for more information.

<hr>
<table style="border:none">
  <tr>  
    <td align="center"><img src="Graphics/mahinsLogo.png" height="250" width="250"></h4></td>
  </tr>
  <tr>  
    <td align="center"><h4>Developed by <br> Md. Mahinur Rahman</h4></td>
  </tr>
</table>

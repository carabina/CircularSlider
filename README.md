# CircularSlider
A powerful Circular Slider. It's written in Swift and it's 100% IBDesignable and IBInspectable.

# Demo

![Slider demo](https://raw.githubusercontent.com/taglia3/CircularSlider/master/Gif/demo.gif)

# Installation

CircularSlider is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'CircularSlider'
```

# Usage
You can use this slider by declaring programmatically or by placing it in your Storyboard file.
All the paramters are IBInspectable, so you can configure the slider directly in the Storyboard file (in the attribute inspector tab) without write any line of code!

![IBInspectable params](https://raw.githubusercontent.com/taglia3/CircularSlider/master/Images/attributeInspector.png =300x)
![IBInspectable params](https://raw.githubusercontent.com/taglia3/CircularSlider/master/Images/storyboardRender.png =300x)


## Delegate
Optionally you can conforms to the methods of the CircularSliderDelegate protocol.

If you want to admit only certain values you can implement this methods:
```swift
optional func circularSlider(circularSlider: CircularSlider, valueForValue value: Float) -> Float
```
With this method you override the actual slider value before the slider is updated.
Example: you want only rounded values:

```swift
func circularSlider(circularSlider: CircularSlider, valueForValue value: Float) -> Float {
return Float(Int(value))
}
```

The other methods you can implement are:

```swift
optional func circularSlider(circularSlider: CircularSlider, didBeginEditing textfield: UITextField)
optional func circularSlider(circularSlider: CircularSlider, didEndEditing textfield: UITextField)
```


## Author

taglia3, matteo.tagliafico@gmail.com

[LinkedIn](https://www.linkedin.com/in/matteo-tagliafico-ba6985a3), Matteo Tagliafico

## License

CircularSpinner is available under the MIT license. See the LICENSE file for more info.
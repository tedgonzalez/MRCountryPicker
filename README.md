# MRCountryPicker

[![CI Status](http://img.shields.io/travis/xtrinch/MRCountryPicker.svg?style=flat)](https://travis-ci.org/xtrinch/MRCountryPicker)
[![Version](https://img.shields.io/cocoapods/v/MRCountryPicker.svg?style=flat)](http://cocoapods.org/pods/MRCountryPicker)
[![License](https://img.shields.io/cocoapods/l/MRCountryPicker.svg?style=flat)](http://cocoapods.org/pods/MRCountryPicker)
[![Platform](https://img.shields.io/cocoapods/p/MRCountryPicker.svg?style=flat)](http://cocoapods.org/pods/MRCountryPicker)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

![screen shot 2016-06-11 at 13 00 05](https://cloud.githubusercontent.com/assets/7256491/15984684/7930c73e-2fd4-11e6-83b8-91d522674a0c.png)

## Usage

Make your UIPickerView a class of MRCountryPicker, set its countryPickerDelegate and implement its didSelectCountryWithName method.

See example: 

```
class ViewController: UIViewController, MRCountryPickerDelegate {

    @IBOutlet weak var countryPicker: MRCountryPicker!
    @IBOutlet weak var countryName: UILabel!
    @IBOutlet weak var countryCode: UILabel!
    @IBOutlet weak var countryFlag: UIImageView!
    @IBOutlet weak var phoneCode: UILabel!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        countryPicker.countryPickerDelegate = self
        countryPicker.showPhoneNumbers = true
        countryPicker.setCountry("SI")
    }
    
    func countryPhoneCodePicker(picker: SwiftCountryPicker, didSelectCountryWithName name: String, countryCode: String, phoneCode: String, flag: UIImage) {
        self.countryName.text = name
        self.countryCode.text = countryCode
        self.phoneCode.text = phoneCode
        self.countryFlag.image = flag
    }

}
```

## Installation

SwiftCountryPicker is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "MRCountryPicker"
```

## Author

Mojca Rojko, mojca.rojko@gmail.com

Made with a little help from my friends over at:  
https://github.com/marmelroy/PhoneNumberKit  
https://github.com/Keyflow/CountryPicker-iOS-Swift  
https://github.com/nicklockwood/CountryPicker

## License

MRCountryPicker is available under the MIT license. See the LICENSE file for more info.

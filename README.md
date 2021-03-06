#CNPPopupController

CNPPopupController is a simple and versatile class for presenting a custom popup in a variety of fashions. It includes a many options for controlling how your popup appears and behaves.

Please feel free to contribute to this project, open issues, make suggestions and submit pull-requests. If you use this project in your app, let me know. I'd love to see what you do with it. 

<p align="center"><img src="https://raw.githubusercontent.com/carsonperrotti/CNPPopupController/master/CNPPopupControllerExample/CNPPopupController.gif"/></p>

## Installation

Available in [Cocoa Pods](http://cocoapods.org/?q=CNPPopupController)

`pod 'CNPPopupController'`

##Usage

(See sample Xcode project in `/CNPPopupControllerExample`)

## Creating a Popup

Create a popup with custom animations and behaviors. Customizations can also be accessed via properties on the `CNPPopupTheme` instance:

	- (instancetype)initWithTitle:(NSAttributedString *)popupTitle
                     contents:(NSArray *)contents
                  buttonTitles:(NSArray *)buttonTitles
       destructiveButtonTitle:(NSAttributedString *)destructiveButtonTitle;

`popupTitle` only accepts an `NSAtributedString` object.

`contents` only accepts an array of `NSAttributedString` and `UIImage` objects.

`buttonTitles` only accepts an array of `NSAttributedString` objects.

`destructiveButtonTitle ` only accepts an `NSAtributedString` object.

---

Note: You may pass `nil` for any of the initializer properties when creating the popup, but **you must assign a `theme` to the popup before showing it!**

A default theme `+ [CNPPopupTheme defaultTheme]` has been created to help you out.
					
## Showing a Popup

`- (void)presentPopupControllerAnimated:(BOOL)flag;`

## Dismissing a Popup

`- (void)dismissPopupControllerAnimated:(BOOL)flag;`

## Customization

A `CNPPopupTheme` instance can be created and assigned to the `theme` property of a `CNPPopupController` instance. 

`@property (nonatomic, strong) UIColor *backgroundColor;`
`@property (nonatomic, assign) CGFloat cornerRadius;`
`@property (nonatomic, strong) UIColor *buttonBackgroundColor;`
`@property (nonatomic, strong) UIColor *destructiveButtonBackgroundColor;`
`@property (nonatomic, assign) CGFloat preferredPopupWidth;`
`@property (nonatomic, assign) CGFloat minimumPopupHeight;`
`@property (nonatomic, assign) CGFloat buttonHeight;`
`@property (nonatomic, assign) CGFloat buttonCornerRadius;`
`@property (nonatomic, assign) UIEdgeInsets popupContentInsets;`
`@property (nonatomic, assign) CNPPopupStyle popupStyle;`
`@property (nonatomic, assign) CNPPopupPresentationStyle presentationStyle;`
`@property (nonatomic, assign) CNPPopupMaskType maskType;`
`@property (nonatomic, assign) BOOL shouldDismissOnBackgroundTouch;`
`@property (nonatomic, assign) CGFloat contentVerticalPadding;`
`@property (nonatomic, assign) UIStatusBarStyle fullscreenStatusBarStyle;`

## Notes

### Deployment
`CNPPopupController ` works on **iOS 7** and **iOS 8**.

### TODO
- Add better rotation support including resizing to fit.
- Add 'blur' option for background mask

##Credits
CNPPopupController was created by [Carson Perrotti](http://carsonperrotti.com), where it's used in the [Joist app](http://joistapp.com).

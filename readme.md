KGModal is an easy drop in control that allows you to display any view in a modal popup. The modal will automatically scale to fit the content view and center it on screen with nice animations!

![](https://raw.github.com/kgn/KGModal/master/Screenshot.jpg)

You supply your own content view and KGModal does the rest:

``` obj-c
[[KGModal sharedInstance] showWithContentView:contentView andAnimated:YES];
```

There are a couple other options but it's purposely designed to be simple and easy to use:

``` obj-c
// Determines if the modal should dismiss if the user taps outside of the modal view
// Defaults to YES
@property (nonatomic) BOOL tapOutsideToDismiss;

// Determines if the close button or tapping outside the modal should animate the dismissal
// Defaults to YES
@property (nonatomic) BOOL animateWhenDismissed;

// The background display style, can be a transparent radial gradient or a transparent black
// Defaults to gradient, this looks better but takes a bit more time to display on the retina iPad
@property (nonatomic) enum KGModalBackgroundDisplayStyle backgroundDisplayStyle;

// The shared instance of the modal
+ (id)sharedInstance;

// Set the content view to display in the modal and display with animations
- (void)showWithContentView:(UIView *)contentView;

// Set the content view to display in the modal and whether the modal should animate in
- (void)showWithContentView:(UIView *)contentView andAnimated:(BOOL)animated;

// Hide the modal with animations
- (void)hide;

// Hide the modal and whether the modal should animate away
- (void)hideAnimated:(BOOL)animated;
```

Check out the ExampleApp to see it in action!
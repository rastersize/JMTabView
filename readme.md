## JMTabView

This is a dark-themed and easy to use tab view created entirely using Core Graphics, so that it is easy to drop-in to your projects and operates smoothly on iOS devices.  The library itself will also be used in Alien Blue's upcoming iOS updates.

## How it looks

Here's what JMTabView looks like:

<img src="http://alienblue.org/github/JMTabView.png" width=477 height=54 />

And on a retina display:

<img src="http://alienblue.org/github/JMTabView-retina.png" width=638 height=120 />

## Usage

A demo project is included in this repository so that you can dive right in.  In brief, to draw the tab view, you can do the following:

`JMTabView * tabView = [[[JMTabView alloc] initWithFrame:frame] autorelease];`

`[tabView setDelegate:self];`

You can then add tab items:

`[tabView addTabItemWithTitle:@"One" icon:[UIImage imageNamed:@"icon1.png"]];`

By implementing the `tabView:didSelectTabAtIndex:` method, you will receive a callback when the tab selection changes.

## Flexibility

You can set the `icon:` to `nil` if you prefer to use text only, or `title:` to `nil` to show icons only.

If you prefer to use JMTabView as a **toolbar** you can use the `setMomentary:` method to change its selection behaviour.

JMTabView also supports the execution of blocks so that you can embed your logic per tab item, like this:

`[tabView addTabItemWithTitle:@"Tab" icon:nil executeBlock:^{
    // do stuff after item has been selected
}];`

## Customisation

You can subclass `JMTabItem` and `JMSelectionView` to completely customize the view of the tabs.  For example, in the inclusive Demo you can see how I've customized the view to render tabs like this:

<img src="http://alienblue.org/github/JMTabView-custom.png" width=639 height=153 />

## Installation

You can either add the built library to your project or you can reference the .h and .m files directly.

## Acknowledgements

This project uses the UIView+Positioning and UIView+Size categories developed by the very talented [Kevin O'Neill](https://github.com/kevinoneill/Useful-Bits).

## License

JMTabView is BSD licensed, so you can freely use it in commercial applications.

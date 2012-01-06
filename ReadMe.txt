PrintWebView

=========================================================================
DESCRIPTION:

PrintWebView demonstrates how to print a UIWebView using a UIViewPrintFormatter. This application is a very primitive Web browser that has printing capability.

The sample is internationalized. See the Localized.strings file in the project's Resources/en.lproj folder.

PrintWebView shows how to:

	* Obtain and use the shared UIPrintInteraction controller.
	* Use a UIViewPrintFormatter to handle formatting and rendering of content in a webview.
	* Use a custom UIPrintPageRenderer to add a header and footer to each page.
	* This example shows how to simply place a header and footer at the top and bottom
	  of the page, positioned relative to the imageable area of the paper. To achieve this
	  set the define SIMPLE_LAYOUT to 1 in MyPrintPageRenderer.h.
	* The code (optionally) demonstrates how to carefully place the content of the view
          so that it is located consistently, independent of the imageable area of the paper,
	  e.g. inset by 1/2 inch from each edge. To achieve this, set the #define SIMPLE_LAYOUT
	  to 0 in MyPrintPageRenderer.h.

=========================================================================
RELATED INFORMATION:



=========================================================================
BUILD REQUIREMENTS:

XCode 3.2.5, Mac OS X 10.6.4 or later


=========================================================================
RUNTIME REQUIREMENTS:

iOS 4.2


=========================================================================
PACKAGING LIST:

MyWebViewController.h
MyWebViewController.m

The MyWebViewController class defines the controller object for the application. This object loads the nib file associated with the user interface.  The MyWebViewController class uses the UIPrintInteractionController to print, using MyPrintPageRenderer, a subclass of the UIPrintPageRenderer class.

MyPrintPageRenderer.h
MyPrintPageRenderer.m
A subclass of the UIPrintPageRenderer used to draw a header and footer on the webpage content being printed. The content of the webpage is being drawn by a UIViewPrintFormatter. MyPrintPageRenderer performs calculations to set the properties of the MyPrintPageRenderer and UIViewPrintFormatter objects so that the header and footer drawn by MyPrintPageRenderer and the content drawn by the UIViewPrintFormatter are located properly.


=========================================================================
CHANGES FROM PREVIOUS VERSIONS:

10/11/2010 - 1.2 Use the same toolbar autoresizingMask for iPad and iPhone.

9/23/2010 - 1.1 Ensure that the toolbar's autoresizingMask is correct so that orientation changes don't lose the toolbar.

9/10/2010 - 1.0 First version.

=========================================================================
Copyright (C) 2010 Apple Inc.  All rights reserved.

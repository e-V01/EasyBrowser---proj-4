#  EasyBrowser - proj 4
This is the code for a simple web browser app called EasyBrowser. It allows users to navigate websites and includes features such as progress tracking, toolbar with refresh and navigation buttons, and a list of predefined websites to choose from.


Explanation:
The ViewController class is a subclass of UIViewController and conforms to the WKNavigationDelegate protocol.
The webView property is an instance of WKWebView, which will be used to display web content.
The progressView property is an instance of UIProgressView, which shows the loading progress of the web page.
The website array stores the predefined websites that the user can choose from.
The loadView() method sets up the webView as the view for the view controller.
The viewDidLoad() method is called after the view has been loaded and is used to set up the navigation bar, toolbar, and initial webpage loading.
The openTapped() method is the action triggered when the user taps the "Open" button. It presents an action sheet with options to open each predefined website.
The openPage(action:) method is the action triggered when the user selects a website from the action sheet. It loads the selected webpage in the webView.
The webView(_:didFinish:) method is called when the web page finishes loading. It sets the view controller's title to the title of the loaded webpage.
The observeValue(forKeyPath:of:change:context:) method is called when the observed key-value changes. Here, it updates the progressView with the estimated progress of the webpage loading.
The webView(_:decidePolicyFor:decisionHandler:) method is called when the web view is about to navigate to a requested URL. It checks if the requested URL's host matches any of the allowed websites. If it does, it allows the navigation; otherwise, it blocks it and shows an alert.


This code provides a basic web browser functionality with the ability to open predefined websites, navigate forward and backward, refresh the page, and display loading progress. It also blocks navigation to websites not listed in the website array.

# Sunrise

## Setting the Internet Explorer version

To set the Internet Explorer version that the WebBrowser control uses, I had to add a registry value.

Otherwise, the WebBrowser control uses an outdated IE version that does not render pages properly.

In the Registry Editor app, I opened the registry key location HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\Main\FeatureControl\FEATURE_BROWSER_EMULATION.

I then added my application name "Sunrise.exe" as a DWORD (32-bit) value. I set the value to 11000 to signify IE version 11.

[Microsoft documentation on FEATURE_BROWSER_EMULATION](https://docs.microsoft.com/en-us/troubleshoot/developer/browsers/development-website/ie-document-modes-faq#how-can-i-configure-browser-emulation-for-web-browser-controls-in-internet-explorer)

After adding this registry value, I saw a dramatic improvement in how web pages rendered.
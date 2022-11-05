# Payload Library for the USB Rubber Ducky by Hak5
This repository contains payloads and extensions for the Hak5 USB Rubber Ducky. Community developed payloads are listed and developers are encouraged to create pull requests to make changes to or submit new payloads.

# About the USB Rubber Ducky and DuckyScript
<b> A "flash drive" that types keystroke injection payloads into unsuspecting devices at incredible speeds. </b>
-   [Purchase the NEW USB Rubber Ducky](https://hak5.org/products/usb-rubber-ducky?variant=39874478932081 "Purchase the NEW USB Rubber Ducky")
-   [Documentation](https://docs.hak5.org/hak5-usb-rubber-ducky/ "Documentation")
-   [Forums](https://forums.hak5.org/forum/111-new-usb-rubber-ducky/ "Forums")
-   [Discord](https://hak5.org/discord "Discord")

[![USB Rubber Ducky](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MiIkRK_o3RBhZzUkrzr%2Fuploads%2FW1Cy0NoSZJhOkaG7gk9t%2Fusb-rubber-ducky-3d-white-bg.png?alt=media&token=7a92ff75-c7ae-4280-b4da-690bef71dac8)](https://hak5.org/products/usb-rubber-ducky)

<p align="center"><i> New USB Rubber Ducky (A+C, DuckyScript 3.0, 2022)</i></p>

## DuckyScript™ 1.0 (Legacy)
Hak5 introduced Keystroke Injection in 2010 with the USB Rubber Ducky™. This technique, developed by Hak5 founder Darren Kitchen, was his weapon of choice for automating mundane tasks at his IT job — fixing printers, network shares and the like.
Today the USB Rubber Ducky is a hacker culture icon, synonymous with the keystroke injection technique it pioneered. It’s found its way into the hearts and toolkits of Cybersecurity and IT pros the world over — including many movies and TV shows!
Core to its success is its simple language, DuckyScript™. Originally just three commands, it could be learned by anyone—regardless of experience—in minutes.

## DuckyScript 3.0
With the new USB Rubber Ducky in 2022, DuckyScript 3.0 has been introduced.
DuckyScript 3.0 is a feature rich, structured programming language. It includes all of the previously available commands and features of the original DuckyScript.
Additionally, DuckyScript 3.0 introduces control flow constructs (if/else if/else), repetition (loops), functions, extensions.
Plus, DuckyScript 3.0 includes many features specific to keystroke injection attack/automation, such as HID & Storage attack modes, OS Detection, [Keystroke Reflection](https://shop.hak5.org/pages/keystroke-reflection "Keystroke Reflection"), jitter and randomization to name a few.
[This documentation](https://docs.hak5.org/hak5-usb-rubber-ducky/ "This documentation") will cover the basics, then introduce each of the new features such that they build upon one another.


<h2><a href="https://payloadstudio.hak5.org"> PayloadStudio</a></h2>
<p align="center">
<a href="https://payloadstudio.hak5.org"><img src="https://cdn.shopify.com/s/files/1/0068/2142/products/payload-studio-icon_180x.png?v=1659135374"></a>
<br/>
<a href="https://hak5.org/products/payload-studio-pro">Become a PayloadStudio Pro</a> and <b> Unleash your hacking creativity! </b>
<br/>
<i>a fully featured IDE for all your DuckyScript development across all your favorite Hak5 tools.</i>
<a href="https://payloadstudio.hak5.org"><img src="https://cdn.shopify.com/s/files/1/0068/2142/files/payload-studio-error-checking_600x.gif"></a>
<br/>
<a href="https://payloadstudio.hak5.org">Try Community Edition FREE</a> 
</p>

## Legal
Payloads from this repository are provided for educational purposes only.  Hak5 gear is intended for authorized auditing and security analysis purposes only where permitted subject to local and international laws where applicable. Users are solely responsible for compliance with all laws of their locality. Hak5 LLC and affiliates claim no responsibility for unauthorized or unlawful use.

USB Rubber Ducky and DuckyScript are the trademarks of Hak5 LLC. Copyright © 2010 Hak5 LLC. All rights reserved. No part of this work may be reproduced or transmitted in any form or by any means without prior written permission from the copyright owner.
USB Rubber Ducky and DuckyScript are subject to the Hak5 license agreement (https://hak5.org/license)
DuckyScript is the intellectual property of Hak5 LLC for the sole benefit of Hak5 LLC and its licensees. To inquire about obtaining a license to use this material in your own project, contact us. Please report counterfeits and brand abuse to legal@hak5.org.
This material is for education, authorized auditing and analysis purposes where permitted subject to local and international laws. Users are solely responsible for compliance. Hak5 LLC claims no responsibility for unauthorized or unlawful use.
Hak5 LLC products and technology are only available to BIS recognized license exception ENC favorable treatment countries pursuant to US 15 CFR Supplement No 3 to Part 740.

## Disclaimer
Generally, payloads may execute commands on your device. As such, it is possible for a payload to damage your device. Payloads from this repository are provided AS-IS without warranty. While Hak5 makes a best effort to review payloads, there are no guarantees as to their effectiveness. As with any script, you are advised to proceed with caution.

## Contributing
Once you have developed your payload, you are encouraged to contribute to this repository by submitting a Pull Request. Reviewed and Approved pull requests will add your payload to this repository, where they may be publically available.

### Please adhere to the following best practices and style guide when submitting a payload.

### Naming Conventions
Please give your payload a unique, descriptive and appropriate name. Do not use spaces in payload, directory or file names. Each payload should be submit into its own directory, with `-` or `_` used in place of spaces, to one of the categories such as exfiltration, phishing, remote_access or recon. Do not create your own category.

### Payload Configuration
In many cases, payloads will require some level of configuration by the end payload user. Be sure to take the following into careful consideration to ensure your payload is easily tested, used and maintained. 

- Abstract configuration(s) for ease of use. Use `DEFINE` where possible.
- Remember to use PLACEHOLDERS for configurable portions of your payload - do not share your personal URLs, API keys, Passphrases, etc...
- Make note of both required and optional configuration(s) in your payload using comments at the top of your payload or "inline" where applicable
<pre>
Example: 
	REM Configuration
	REM REQUIRED - Provide URL used for <something> 
	DEFINE MY_TARGET_URL example.com
	REM OPTIONAL - How long until payload starts; default 5s
	DEFINE BOOT_DELAY 5000
	REM End Configuration
	...
	DELAY 5000
	...
	STRING MY_TARGET_URL
	...
</pre>
### Payload Documentation 
Payloads should begin with `REM` comments specifying the title of the payload, the author, the target, and a brief description.
<pre>
Example:
	REM Title: Example Payload
	REM Author: Korben Dallas
	REM Description: Opens hidden powershell and ...
	REM Target: Windows 10
	REM Props: Hak5, Darren Kitchen, 
	REM Version: 1.0
	REM Category: General
</pre>

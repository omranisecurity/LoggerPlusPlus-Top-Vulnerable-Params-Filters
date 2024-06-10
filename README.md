# LoggerPlusPlus-Top-Vulnerable-Params-Filters
Logger++ is a multithreaded logging extension for Burp Suite. In addition to logging requests and responses from all Burp Suite tools, the extension allows advanced filters to be defined to highlight interesting entries or filter logs to only those which match the filter.

This repository has been created by collecting parameters suspected to be vulnerable to various attacks, to help you quickly and easily identify suspicious endpoints while working with Burp Suite and Logger++.

## Top Parameters of XSS Vulnerability
```
Request.Query == /\b(?:q|s|search|lang|keyword|query|page|keywords|year|view|email|type|name|p|month|image|list_type|url|terms|categoryid|key|begindate|enddate)\b/
```

## Top Parameters of SSRF Vulnerability
```
Request.Query == /\b(?:access|admin|dbg|debug|edit|grant|test|alter|clone|create|delete|disable|enable|exec|execute|load|make|modify|rename|reset|shell|toggle|adm|root|cfg|dest|redirect|uri|path|continue|url|window|next|data|reference|site|html|val|validate|domain|callback|return|page|feed|host|port|to|out|view|dir|show|navigation|open|file|document|folder|pg|php_path|style|doc|img|filename)\b/
```

## Top Parameters of LFI Vulnerability
```
Request.Query == /\b(?:cat|dir|action|board|date|detail|file|download|path|folder|prefix|include|page|inc|locate|show|doc|site|type|view|content|document|layout|mod|conf|root|pg|style|pdf|template|php_path|name|url)\b/
```

## Top Parameters of SQL Injection Vulnerability
```
Request.Query == /\b(?:id|page|dir|search|category|file|class|url|news|item|menu|lang|name|ref|title|view|topic|thread|type|date|form|join|main|nav|region|select|report|role|update|query|user|sort|where|params|process|row|table|from|sel|results|sleep|fetch|order|keyword|column|field|delete|string|number|filter)\b/
```

## Top Parameters of RCE Vulnerability
```
Request.Query == /\b(?:cmd|exec|command|execute|ping|query|jump|code|reg|do|func|arg|option|load|process|step|read|function|req|feature|exe|module|payload|run|print|daemon|upload|dir|download|log|ip|cli)\b/
```

## Top Parameters of Open Redirect Vulnerability
```
Request.Query == /\b(?:next|url|target|rurl|dest|destination|redir|redirect_url|redirect_uri|redirect|cgi-bin/redirect.cgi|out|view|login?to|image_url|go|return|return_to|checkout_url|continue|Lmage_url|Open|callback|checkout|data|domain|feed|file|file_name|file_url|folder|folder_url|forward|from_url|goto|host|html|img_url|load_file|load_url|login_url|logout|navigation|next_page|page|page_url|port|redirect_to|reference|return_path|return_url|rt|show|site|to|uri|val|validate|window)\b/
```

## Top Parameters of IDOR Vulnerability
```
Request.Query == /\b(?:id|user|account|number|order|no|doc|key|email|group|profile|edit|report)\b/
```

## Top Parameters of SSTI Vulnerability
```
Request.Query == /\b(?:template|preview|id|view|activity|name|content|redirect)\b/
```

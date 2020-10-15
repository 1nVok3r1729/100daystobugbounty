## Notes on Open Redirect:

If you need better understanding on open redirection vulnerabilty read this awesome [blog](https://medium.com/bugbountywriteup/open-redirection-leads-to-a-bounty-d94029e11d17) by [@impratikdabhi](https://twitter.com/impratikdabhi). You can get more than 100 h1 open redirect reports from [here](https://github.com/reddelexc/hackerone-reports/blob/master/tops_by_bug_type/TOPOPENREDIRECT.md).

### gf-pattern:
Get it [here](https://github.com/muhe7/gf-pattern).

### One-Liner:
`
▶ gau http://google.com -s  | head -n 5000 > google.txt; cat google.txt | sort -u | grep -a -i \=http > google_redirects.txt
`

`
▶ waybackulrs google.com | gf open-redirect | tee google.txt
`







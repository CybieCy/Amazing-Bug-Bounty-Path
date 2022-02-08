![jpg_20220208_111419_0000](https://user-images.githubusercontent.com/94240494/152926460-3e6da09c-3f4f-464e-aa7f-35cc8087178e.jpg)

[![image](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/NandanLohitaksh) [![](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/lohitakshnandan) [![](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lohitakshnandan)

</div>

# Amazing Bug Bounty Path
## Mindset
If you are beginning bug bounty hunting, you will need to know that it will take time to learn the bug hunting skills. You need to have the patience and determination to continue hunting even though you might not see successful results quickly. The bug bounty field is crowded and competitive, hence you will require hardwork, dedication, lateral thinking to persist on. Hunting is about learning and acting noob all the time. Everyone starts from somewhere.

> From Tommy (dawgyg) DeVoss: If you have the ability to look at a web application and think of ways to break the application, then you can give it a shot. For some people it can be a very slow start to the process, and others will start finding bugs right after they begin. A very important thing to remember when doing bug bounties is to not get depressed / upset if it takes you longer to find valid bugs etc. Not everyone is going to find bugs every time they sit down to hack. And its very common to go days, weeks or even months with out finding bugs. Don't compare your own success or failures to others. Because as with anything else, there will always be someone better than you, and others worse than you. So setting your own goals and working to acheive them can be very important.

<b>Rewards.</b> The lessons and knowledge learned are the only rewards that are within your control. So if you are a beginner, you should set the goal of learning about the vulnerabilities and techniques to exploit them rather than how much money you should make.

<b>Responsiblity.</b> Do not disclose an issue if the counterparty have not agreed to do so.

## Learning
<b>Web Application basics</b>. Learn how a request works, HTTP headers, JSON requests, how a browser works, how they communicate and send data to the servers, DNS etc. https://developer.mozilla.org/en-US/docs/Web

<b>Common scope vulnerabilities.</b> You will need to know common scope vulnerabilities such as Remote Code Execution (RCE), Cross Site Request Forgery (CSRF), Cross Site Scripting (XSS), Injections (SQL, Command etc.), Clickjacking, Open Redirects, etc.

<b>Read blogs.</b> Learn new techniques from other bug bounty hunters so that you can test it out during your testing.

>If you are new to Bug Bounty program, you might not feel confident that you can find something a public program. This is something that a lot of hackers are struggling with. If you haven’t found a lot of security vulnerabilities yet, it might payoff to practice on Capture The Flag (CTF). Exploiting something for the first time is difficult and eye-opening. Apply the same structure if you would apply when looking in real targets as this help you a build a solid foundation and will help you to become an amazing hacker. Use bug bounty as a way to expand your knowledge and not as a race. Write simple scripts and use available tools to expand the process of expanding attack surface [...] Understand the web application and figure out what assets the web application are trying to protect. Think like an engineer of the web application. (Jobert Abma, Hackerone Cofounder)

<b>Learn how to make and then break.</b> You need to know how a web or mobile application is developed first so that you can understand how the thing works and hence how it can be broken down. This is beneficial for your long-term development rather than being a hunter that only knows how to send payloads (obtained from internet). Build a few web applications to understand how the web architecture works.

> From <a href="https://twitter.com/spaceraccoonsec/status/1250403032971407360?s=20"> Spaceraccoon's tweet</a>: To be blunt, I don't automate. I tried building a pipeline and failed. You can succeed just by learning the fundamentals. Check out @PortSwigger's web academy, watch @NahamSec's stream, read @Hacker0x01 disclosures. And learn how to build what you're hacking.

### Training Platforms
- [BugBountyHunter](https://www.bugbountyhunter.com/): 
  - Simulates Opacity: The platform simulates a more realistic bug hunting experience where you need to explore and understand each features to find bugs. You do not know beforehand on whether the features have bugs or not (and what kind of vulnerabilities).
  - Community: Members share resources and help each other.
  - Zseano Methodology: Download from https://www.bugbountyhunter.com/methodology/

## Testing Strategies
<b>Scope your Testing.</b> You do not want to test the applications for different vulnerabilities in an unstructured manner because this often results in shallow testing or makes you feel that you have already search for everything. If you are stuck with your testing, ask yourself what you are testing on. Set a SMART goal - specify what the vulnerability you are targeting, the hard deadline for completing the testing, etc. This strategy will help you to know which resources to look for and specific questions to ask your peers. You can also prioritize on what to look for based on the goal.

````Example of a goal: For the next 4 hours, I will test on feature X for SQL Injection.````

<b>Choosing programs with Larger Scope.</b> You want to choose a program that uses something that you are familiar with. If not, then you must ask yourself whether this is something you will like to learn. Larger scope is better because the researchers will not concentrate on the same targets and some things might be overlooked.

> From Tommy (dawgyg) DeVoss: When it comes to picking a program to start there are several things to consider. The first, and most important, is picking a program that employs the kind of stack / architecture you may be familiar with, or have a desire to learn and attack [...] Next you are going to want to consider the scope. When I look at a program to decide if I want to spend any time on it, I look for programs with either large scopes (such as wild card domains, and the more domains the better) or with web apps that are very complex. I personally love huge scopes, since it kind of helps to spread out the researchers a bit. 

<b>Test the uncommon attack vectors.</b> This requires you to do more in depth work in understanding how the application works (in terms of technologies and business functions). Ask yourself whether the bug that you are looking for are already tested automatically by a conventional scanner. For example, if you test a normal XSS payload on the common attack vectors such as input boxes etc., the chances are that many hunters have done it. Ask yourself whether there are other ways to trigger the XSS payload in an unexpected attack vector.

> From Inti: Edge-cases like that is what I love. If I have a secret, that is the one. Do not look where everyone is looking, because you will get a duplicate [...] My advice: if you are a researcher and want to secure your payout for the next 5-10 years, start looking for custom bugs, logical flaws, and other things scanners or other researchers do not look into. That can lead to more impact, you will find new types of vulnerabilities, you can get speaker events, write blog posts about it, opportunities are plenty. It is more about your mindset and being open-minded to try stupid stuff or something unknown and not follow a checklist.

<b>Look for impactful bugs.</b> Try to submit bugs which are impactful and easy to understand. Choose quality over quantity. Many successful hunters read the programme policies first before they start looking for vulnerabilities.

<b>Do the unexpected action</b> Don't submit what the application is expecting. Instead, start thinking about the things that the developers did not consider.

>From Peter Yaworski: <ul><li>For a text editor, if you can insert html, try doubling up on html attributes, like two hrefs in an anchor tag, or extra quotes like the markdown example.</li><li>When submitting forms, use a tool or proxy to remove parameters (for Firefox, tamperdata is a great one). On the same note, if a site is using JavaScript to validate input before it is submitted to the server, use the proxy to change the values after they are validated in the event the developer just relied on the JavaScript.</li><li>Combining steps to create vulnerability. Again, with the Hackerone markdown example, having the hanging single quote combined with additional html later in the page with a single quote would create vulnerability. With Google's program, they include a multiplier whereby if you need multiple steps and you can actually demonstrate that all the steps are achievable, they'll increase your reward.</li><li>Consider where the vulnerability might actually show up. For example, Shopify's disclosure program states that it excludes vulnerabilities on your own store or cart (I learned the hard way from over excitement...). BUT, some of the fields that are used to create your store are used externally as well. There is an disclosure report indicating that the currency formatting field allowed for XSS injection. At first glance, you would think this shows up on the store page so who cares. BUT, Shopify provides integration with Facebook and Twitter using that same field and actually rendered the XSS resulting in a $500 bounty</li></ul>

## Resources
### Books
<ul>
  <li>The Web Application Hacker’s Handbook</li>
  <li><a href="https://www.owasp.org/index.php/OWASP_Testing_Project">OWASP Testing Guide</a></li>
  <li>The Tangled Web: A Guide to Securing Modern Web Applications</li>
  <li>Web Hacking 101</li>
  <li>Breaking into Information Security</li>
  <li>Mastering Modern Web Penetration Testing</li>
  <li>The Mobile Application Hacker's Handbook</li>
  <li><a href="https://www.owasp.org/index.php/OWASP_Mobile_Security_Testing_Guide">OWASP Mobile Security Testing Guide (MSTG)</a></li>
</ul>

### Write Ups & Authors
- [sakurity.com/blog](http://sakurity.com/blog)  -  by [Egor Homakov](https://twitter.com/homakov)
- [respectxss.blogspot.in](http://respectxss.blogspot.in/)  -  by [Ashar Javed](https://twitter.com/soaj1664ashar)
- [labs.detectify.com](http://labs.detectify.com/)  -  by [Frans Rosén](https://twitter.com/fransrosen)
- [cliffordtrigo.info](https://www.cliffordtrigo.info/)  -  by [Clifford Trigo](https://twitter.com/MrTrizaeron)
- [stephensclafani.com](http://stephensclafani.com/)  -  by [Stephen Sclafani](https://twitter.com/Stephen)
- [sasi2103.blogspot.co.il](http://sasi2103.blogspot.co.il/)  -  by [Sasi Levi](https://twitter.com/sasi2103)
- [pwnsecurity.net](http://www.pwnsecurity.net/)  -  by [Shashank](https://twitter.com/cyberboyIndia)
- [breaksec.com](https://www.breaksec.com/)  -  by [Nir Goldshlager](https://twitter.com/Nirgoldshlager)
- [pwndizzle.blogspot.in](http://pwndizzle.blogspot.in/)  -  by [Alex Davies](https://twitter.com/pwndizzle)
- [c0rni3sm.blogspot.in](http://c0rni3sm.blogspot.in/)  -  by [yappare](https://twitter.com/yappare)
- [exploit.co.il/blog](http://exploit.co.il/blog/)  -  by [Shai rod](https://twitter.com/NightRang3r)
- [ibreak.software](https://ibreak.software/)  -  by [Riyaz Ahemed Walikar](https://twitter.com/riyazwalikar)
- [panchocosil.blogspot.in](http://panchocosil.blogspot.in/)  -  by [Francisco Correa](https://twitter.com/@panchocosil)
- [breakingmesh.blogspot.in](http://breakingmesh.blogspot.in/)  -  by [Sahil Sehgal](https://twitter.com/xXSehgalXx)
- [websecresearch.com](http://www.websecresearch.com/)  -  by [ Ajay Singh Negi](https://twitter.com/ajaysinghnegi)
- [securitylearn.net](http://www.securitylearn.net/about/)  -  by [Satish Bommisetty](https://twitter.com/satishb3)
- [secinfinity.net](http://www.secinfinity.net/)  -  by Prakash Sharma
- [websecuritylog.com](http://www.websecuritylog.com/)  -  by [jitendra jaiswal](https://twitter.com/jeetjaiswal22)
- [medium.com/@ajdumanhug](https://medium.com/@ajdumanhug) - by [Allan Jay Dumanhug](https://www.twitter.com/ajdumanhug)
- [Web Hacking 101](https://leanpub.com/web-hacking-101) - by [Peter Yaworski](https://twitter.com/yaworsk)


### Platforms
- [YesWeHack](https://yeswehack.com/)
- [intigriti](https://intigriti.com/)
- [HackerOne](https://hackerone.com/)
- [Bugcrowd](https://bugcrowd.com/)
- [Cobalt](https://cobalt.io/)
- [Bountysource](https://www.bountysource.com/)
- [Bounty Factory](https://bountyfactory.io/)
- [Coder Bounty](http://www.coderbounty.com/)
- [FreedomSponsors](https://freedomsponsors.org/)
- [FOSS Factory](http://www.fossfactory.org/)
- [Synack](https://www.synack.com/)
- [HackenProof](https://hackenproof.com/)
- [Detectify](https://cs.detectify.com/)
- [Bugbountyjp](https://bugbounty.jp/)
- [Safehats](https://safehats.com/)
- [BugbountyHQ](https://www.bugbountyhq.com/)
- [Hackerhive](https://hackerhive.io/)
- [Hacktrophy](https://hacktrophy.com/)
- [AntiHACK](https://www.antihack.me/)
- [CESPPA](https://www.cesppa.com/)

### Available Programs
- [123Contact Form](http://www.123contactform.com/security-acknowledgements.htm)
- [99designs](https://hackerone.com/99designs)
- [Abacus](https://bugcrowd.com/abacus)
- [Acquia](mailto:security@acquia.com)
- [ActiveCampaign](mailto:security@activecampaign.com)
- [ActiveProspect](mailto:security@activeprospect.com)
- [Adobe](https://hackerone.com/adobe)
- [AeroFS](mailto:security@aerofs.com)
- [Airbitz](https://cobalt.io/airbitz)
- [Airbnb](https://hackerone.com/airbnb)
- [Algolia](https://hackerone.com/algolia)
- [Altervista](http://en.altervista.org/feedback.php?who=feedback)
- [Altroconsumo](https://go.intigriti.com/altroconsumo)
- [Amara](mailto:security@amara.org)
- [Amazon Web Services](mailto:aws-security@amazon.com)
- [Amazon.com](mailto:security@amazon.com)
- [ANCILE Solutions Inc.](https://bugcrowd.com/ancile)
- [Anghami](https://hackerone.com/anghami)
- [ANXBTC](https://cobalt.io/anxbtc)
- [Apache httpd](https://hackerone.com/ibb-apache)
- [Appcelerator](mailto:Infosec@appcelerator.com)
- [Apple](mailto:product-security@apple.com)
- [Apptentive](https://www.apptentive.com/contact)
- [Aptible](mailto:security@aptible.com)
- [Ardour](http://tracker.ardour.org/my_view_page.php)
- [Arkane](https://go.intigriti.com/arkanenetwork)
- [ARM mbed](mailto:whitehat@polarssl.org)
- [Asana](mailto:security@asana.com)
- [ASP4all](mailto:support@asp4all.nl)
- [AT&T](https://bugbounty.att.com/bugform.php)
- [Atlassian](https://securitysd.atlassian.net/servicedesk/customer/portal/2)
- [Attack-Secure](mailto:admin@attack-secure.com)
- [Authy](mailto:security@authy.com)
- [Automattic](https://hackerone.com/automattic)
- [Avast!](mailto:bugs@avast.com)
- [Avira](mailto:vulnerabilities@avira.com)
- [AwardWallet](https://cobalt.io/awardwallet)
- [Badoo](https://corp.badoo.com/en/security/#send_bid)
- [Barracuda](https://bugcrowd.com/barracuda)
- [Base](https://go.intigriti.com/base)
- [Basecamp](mailto:security@basecamp.com)
- [Beanstalk](https://wildbit.wufoo.com/forms/wildbit-security-response)
- [BillGuard](https://cobalt.io/billguard)
- [Billys Billing](https://cobalt.io/billys-billing)
- [Binary.com](https://hackerone.com/binary)
- [Binary.com Cashier](https://hackerone.com/binary_cashier)
- [BitBandit.eu](https://cobalt.io/bitbandit-eu)
- [Bitcasa](mailto:security@bitcasa.com)
- [BitCasino](https://cobalt.io/bitcasino)
- [BitGo](https://cobalt.io/bitgo)
- [BitHealth](https://cobalt.io/bithealth)
- [BitHunt](https://hackerone.com/bithunt)
- [BitMEX](https://cobalt.io/bitmex)
- [Bitoasis](https://cobalt.io/bitoasis)
- [Bitpagos](https://cobalt.io/bitpagos)
- [Bitrated](https://cobalt.io/bitrated)
- [Bitreserve](https://cobalt.io/bitreserve)
- [Bitspark](https://cobalt.io/bitspark)
- [Bitwage](https://cobalt.io/bitwage)
- [BitWall](mailto:request@bitwall.io)
- [BitYes](https://cobalt.io/bityes)
- [BlackBerry](https://global.blackberry.com/secure/report-an-issue/en.html)
- [Blackboard](mailto:learnsecurity@blackboard.com)
- [Blackphone](https://bugcrowd.com/blackphone)
- [Blesta](mailto:security@blesta.com)
- [Block.io](https://hackerone.com/blockio)
- [Block.io, Inc.](https://cobalt.io/block-io-inc)
- [Blockchain.info](https://cobalt.io/blockchain-info)
- [BlockScore](https://cobalt.io/blockscore)
- [Bookfresh](https://hackerone.com/bookfresh)
- [Box](mailto:security-reports@box.com)
- [Braintree](mailto:security@braintreepayments.com)
- [Brussels Airlines](https://go.intigriti.com/brusselsairlines)
- [BTC_sx](https://cobalt.io/btc-sx)
- [Buffer](mailto:security@bufferapp.com)
- [BX.in.th](https://cobalt.io/bx-in-th)
- [C2FO](https://hackerone.com/c2fo)
- [Campaign Monitor](https://help.campaignmonitor.com/contact)
- [CARD.com](https://bugcrowd.com/card)
- [Catchafire](https://cobalt.io/catchafire)
- [Caviar](https://hackerone.com/caviar)
- [CCBill](mailto:bugrewards@ccbill.com)
- [CERT/CC](https://hackerone.com/cert)
- [Certly](https://hackerone.com/certly)
- [ChainPay](https://cobalt.io/chainpay)
- [ChangeTip](https://cobalt.io/changetip)
- [Chargify](https://bugcrowd.com/chargify)
- [Chromium Project](https://code.google.com/p/chromium/issues/entry?template=Security%20Bug)
- [Circle](https://cobalt.io/circle)
- [CircleCI](mailto:security@circleci.com)
- [Cisco](http://www.cisco.com/web/about/security/psirt/security_vulnerability_policy.html#roosfassv)
- [ClickUp](https://clickup.com/bug-bounty)
- [Clojars](mailto:contact@clojars.org)
- [CloudFlare](https://hackerone.com/cloudflare)
- [Cobalt](https://cobalt.io/cobalt)
- [Code Climate](mailto:security@codeclimate.com)
- [CodeIgniter](https://hackerone.com/codeigniter)
- [CodePen](https://bugcrowd.com/codepen)
- [Coin Republic](https://cobalt.io/coin-republic)
- [Coin.Space](https://hackerone.com/coinspace)
- [Coinage](https://cobalt.io/coinage)
- [Coinbase](https://hackerone.com/coinbase)
- [CoinDaddy](https://cobalt.io/coindaddy)
- [Coinkite](mailto:feedback@coinkite.com?subject=%5BVulnerability%5D%20-%20)
- [Coinport](https://cobalt.io/coinport)
- [coins.ph](https://cobalt.io/coins-ph)
- [Cointrader.net](https://cobalt.io/cointrader-net)
- [Coinvoy](https://cobalt.io/coinvoy)
- [Collishop](https://go.intigriti.com/collishop)
- [Colruyt](https://go.intigriti.com/colruyt)
- [Compose](mailto:security@compose.io)
- [concrete5](https://hackerone.com/concrete5)
- [Constant Contact](mailto:vulnerability@constantcontact.com)
- [Counterparty](https://cobalt.io/counterparty)
- [Coupa](mailto:security@coupa.com)
- [Coursera](https://hackerone.com/coursera)
- [cPanel](mailto:security@cpanel.net)
- [cPaperless](mailto:support@cPaperless.com)
- [Crix.io](https://cobalt.io/crixio)
- [Cross Border Fines](https://go.intigriti.com/crossborderfines)
- [CrowdShield](https://crowdshield.com/bug-bounty-list.php?bug_bounty_program=crowdshield)
- [Cryptocat](https://github.com/cryptocat/cryptocat/issues)
- [Cupcake](mailto:security@cupcake.io)
- [CustomerInsight](mailto:admin@customerinsight.ca)
- [Cylance](https://hackerone.com/cylance)
- [Dato Capital](mailto:security%40datocapital.com)
- [Detectify](mailto:disclosure@detectify.com)
- [De Volkskrant](https://go.intigriti.com/devolkskrant)
- [Delen Private Bank](https://go.intigriti.com/delen)
- [DigitalOcean](mailto:security@digitalocean.com)
- [DigitalSellz](https://hackerone.com/digitalsellz)
- [Django](https://hackerone.com/django)
- [Doorkeeper](mailto:info@doorkeeper.jp)
- [DoSomething](https://cobalt.io/dosomething)
- [DPD](mailto:security@dpd.zendesk.com)
- [Dragon King](https://hackenproof.com/neverdie/dragon-king)
- [Dreambaby](https://go.intigriti.com/dreamland)
- [Dreamland](https://go.intigriti.com/dream)
- [Dropbox](https://hackerone.com/dropbox)
- [Dropbox Acquisitions](https://hackerone.com/dropbox-acquisitions)
- [Drupal](https://www.drupal.org/node/101494)
- [eBay](http://pages.ebay.com/securitycenter/Researchers.html)
- [Eclipse](mailto:security@eclipse.org)
- [eHealth Hub VZN KUL](https://go.intigriti.com/ehealthhubvznkul)
- [EMC](mailto:security_alert@emc.com)
- [Enano](mailto:security@enanocms.org)
- [Engine Yard](mailto:security@engineyard.com)
- [Envoy](https://hackerone.com/envoy)
- [Eobot](https://cobalt.io/eobot)
- [EthnoHub](mailto:security@ethnohub.com)
- [Etsy](https://www.etsy.com/bounty)
- [EVE](mailto:security@ccpgames.com)
- [Event Espresso](http://eventespresso.com/report-a-security-vulnerability)
- [Everitoken](https://hackenproof.com/everitoken/everitoken-blockchain)
- [Evernote](mailto:security@evernote.com)
- [EURid](https://go.intigriti.com/eurid)
- [Expatistan](mailto:gerardo@expatistan.com)
- [ExpressionEngine](https://hackerone.com/expressionengine)
- [Ezbob](https://cobalt.io/ezbob)
- [Facebook](https://www.facebook.com/whitehat)
- [Faceless](https://hackerone.com/faceless)
- [Factlink](https://hackerone.com/factlink)
- [FanFootage](https://hackerone.com/fanfootage)
- [FastSlots](https://cobalt.io/fastslots)
- [Flash](https://hackerone.com/flash)
- [Flood](mailto:support@flood.io)
- [Flow Dock](mailto:security@flowdock.com)
- [Flox](https://hackerone.com/flox)
- [Fluxiom](mailto:security@fluxiom.com)
- [Fog Creek](http://www.fogcreek.com/contact)
- [FormAssembly](mailto:security@formassembly.com)
- [Founder Bliss](https://cobalt.io/founder-bliss)
- [Foursquare](mailto:security@foursquare.com)
- [Freelancer](mailto:security-reporting@freelancer.com)
- [Gallery](mailto:security@galleryproject.org)
- [Gamma](mailto:security-alert@intergamma.nl)
- [Gemfury](mailto:security@gemfury.com)
- [General Motors](https://hackerone.com/gm)
- [GhostMail](https://hackerone.com/gmguys)
- [GitHub](https://bounty.github.com/submit-a-vulnerability.html)
- [GitLab](https://hackerone.com/gitlab)
- [GlassWire](https://hackerone.com/glasswire)
- [Gliph](mailto:security@gli.ph)
- [GlobaLeaks](https://hackerone.com/globaleaks)
- [Google PRP](mailto:security-patches@google.com)
- [Google VRP](https://www.google.com/about/appsecurity/reward-program/index.html)
- [Grammarly](https://hackerone.com/grammarly)
- [Gratipay](https://hackerone.com/gratipay)
- [GreenAddress](https://cobalt.io/greenaddress)
- [Greenhouse.io](https://hackerone.com/greenhouse)
- [Grok Learning](mailto:security@groklearning.com)
- [HackenProof](https://hackenproof.com/hacken/hackenproof)
- [HackerOne](https://hackerone.com/security)
- [Harmony](mailto:security@collectiveidea.com)
- [Heroku](https://bugcrowd.com/heroku)
- [Hex-Rays](mailto:bugbounty@hex-rays.com)
- [Hive Wallet](https://cobalt.io/hive-wallet)
- [Hootsuite](mailto:security@hootsuite.com)
- [HTC](mailto:security@htc.com)
- [Huawei](mailto:psirt@huawei.com)
- [Hubdia](https://hackerone.com/hubdia)
- [Humble Bundle](https://bugcrowd.com/humblebundle)
- [IAM KU Leuven](https://go.intigriti.com/kuleuvenlogin)
- [Ian Dunn](https://hackerone.com/iandunn-projects)
- [IBM](https://www.ibm.com/scripts/contact/contact/us/en/security_vulnerabilities)
- [ICEcoder](https://bugcrowd.com/icecoder)
- [Iconfinder](mailto:support@iconfinder.com)
- [Ifixit](mailto:security@ifixit.com)
- [Imgur](https://hackerone.com/imgur)
- [ImpressPages](https://cobalt.io/impresspages)
- [Indeed](https://bugcrowd.com/indeed)
- [Independent Reserve](https://cobalt.io/independent-reserve)
- [Informatica](https://hackerone.com/informatica)
- [IntegraXor](http://www.integraxor.com/support.html)
- [Internetwache](mailto:security@internetwache.org)
- [InVision](https://hackerone.com/invision)
- [IRCCloud](https://hackerone.com/irccloud)
- [itBit Exchange](https://hackerone.com/itbit)
- [ITRP](mailto:security@itrp.com)
- [itsme](https://go.intigriti.com/itsme)
- [joola.io](https://hackerone.com/joola-io)
- [Joomla](http://vel.joomla.org/submit-vel)
- [JRuby](mailto:security@jruby.org)
- [jsDelivr](https://hackerone.com/jsdelivr)
- [Juniper](mailto:sirt@juniper.net)
- [Kadira](https://hackerone.com/kadira)
- [Kaneva](mailto:security@kaneva.com)
- [Kayako](http://my.kayako.com/Tickets/Submit)
- [Kenna](https://bugcrowd.com/riskio)
- [Keybase](https://hackerone.com/keybase)
- [Khan Academy](https://hackerone.com/khanacademy)
- [SKB Kontur](https://kontur.ru/.well-known/security.txt)
- [Kraken](mailto:bugbounty@kraken.com)
- [Kinepolis](https://go.intigriti.com/kinepolis)
- [Kuna](https://hackenproof.com/kuna/kuna-crypto-exchange)
- [Lancor Income](https://cobalt.io/lancor-income)
- [LastPass](mailto:security@lastpass.com)
- [LaunchKey](mailto:security@launchkey.com)
- [Lean Testing](https://hackerone.com/leantesting)
- [Librato](mailto:security@librato.com)
- [LibSass](https://hackerone.com/libsass)
- [Liferay](mailto:security@liferay.com)
- [Line](https://bugbounty.linecorp.com/en/)
- [LinkedIn](mailto:security@linkedin.com)
- [LiveEnsure](http://www.liveensure.com/contact.php)
- [LocalBitcoins](https://cobalt.io/localbitcoins)
- [Localize](https://hackerone.com/localize)
- [Logentries](mailto:security@logentries.com)
- [Lookout](mailto:security@lookout.com)
- [Magento](mailto:security@magento.com)
- [MAGIX](mailto:security@magix.net)
- [Mahara](mailto:security@mahara.org)
- [MaiCoin](https://cobalt.io/maicoin)
- [Mail.Ru](https://hackerone.com/mailru)
- [Mailbird](https://cobalt.io/mailbird)
- [MailChimp](http://mailchimp.com/about/security-response/)
- [ManageBGL](https://cobalt.io/managebgl)
- [ManageWP](mailto:security@managewp.com)
- [MapLogin](https://hackerone.com/maplogin)
- [Marietje Schaake](https://go.intigriti.com/marietjeschaake)
- [Marktplatts](https://hackerone.com/marktplaats)
- [Mavenlink](https://hackerone.com/mavenlink)
- [Maximum](https://hackerone.com/maximum)
- [MCProHosting](https://bugcrowd.com/mcprohostings)
- [MEGA](mailto:bugs@mega.co.nz)
- [Mercury](https://cobalt.io/mercury)
- [Meteor](https://hackerone.com/meteor)
- [meXBT](https://cobalt.io/mexbt)
- [Microsoft](mailto:secure@microsoft.com)
- [Mimecast](mailto:disclosure@mimecast.com)
- [Mobile Vikings](https://go.intigriti.com/mobilevikings)
- [Mobile Vikings](https://hackerone.com/mobilevikings)
- [Modus CSR](mailto:security@moduscsr.com)
- [MoneyBird](mailto:security@moneybird.com)
- [MoneyStream](https://hackerone.com/moneystream)
- [Moodle](mailto:security@moodle.org)
- [Motorola Solutions](mailto:security@motorolasolutions.com)
- [Mozilla](https://www.mozilla.org/en-US/security/bug-bounty/)
- [mynxt.info](https://cobalt.io/mynxt-info)
- [NCSC](mailto:cert@ncsc.nl)
- [Nearby Live](https://hackerone.com/nearby)
- [Nest](mailto:security@nest.com)
- [Netflix](mailto:security-report@netflix.com)
- [Neverdie Smart Contract](https://hackenproof.com/neverdie/neverdie-smart-contract)
- [Neverdie Web](https://hackenproof.com/neverdie/neverdie-web)
- [Nexmo](https://cobalt.io/nexmo)
- [Nexuzhealth](https://go.intigriti.com/nexushealth)
- [Nexuzhealth Web PACS](https://go.intigriti.com/nexuzhealthwebpacs)
- [Nginx](https://hackerone.com/ibb-nginx)
- [Nitrous](mailto:security@nitrous.io)
- [Nokia Networks](mailto:security-alert@nokia.com)
- [NoPass](https://cobalt.io/nopass)
- [NZRS](mailto:security@nzrs.net.nz)
- [Offensive Security](mailto:security@offensive-security.com)
- [ok.ru](https://hackerone.com/ok)
- [OKCoin](https://cobalt.io/okcoin)
- [OkCupid](https://hackerone.com/okcupid)
- [Olark](mailto:security@olark.com)
- [OneSpan Mobile](https://go.intigriti.com/vascomobileproducts)
- [OneSpan Server Products](https://go.intigriti.com/vascoserver-sideproducts)
- [Opal Cryptocurrency](https://cobalt.io/opal-cryptocurrency)
- [Openfolio](https://hackerone.com/openfolio)
- [OpenSSL](https://hackerone.com/ibb-openssl)
- [OpenStack](https://security.openstack.org/#how-to-report-security-issues-to-openstack)
- [OpenText](mailto:otst@opentext.com)
- [Opera](https://bugs.opera.com/wizarddesktop)
- [Optimizely](https://cobalt.io/optimizely)
- [Oracle](mailto:secalert_us@oracle.com)
- [ownCloud](https://hackerone.com/owncloud)
- [PagerDuty](mailto:security@pagerduty.com)
- [Panasonic Avionics](https://hackerone.com/panasonic-aero)
- [Pantheon](https://bugcrowd.com/pantheon)
- [Panzura](mailto:security@panzura.com)
- [Paragon Initiative Enterprises](https://hackerone.com/paragonie)
- [Paychoice](mailto:security@paychoice.com.au)
- [PayMill](mailto:security@paymill.com)
- [PayPal](mailto:https://www.paypal.com/bugbounty/register)
- [Paytm](https://bugbounty.paytm.com)
- [Perl](https://hackerone.com/ibb-perl)
- [Phabricator](https://hackerone.com/phabricator)
- [PHP](https://bugs.php.net/report.php)
- [Pidgin](mailto:security@pidgin.im)
- [PikaPay](mailto:security@pikapay.com)
- [PinoyHackNews](mailto:admin@pinoyhacknews.com)
- [Pinterest](https://bugcrowd.com/pinterest)
- [Piwik Open Source Analytics](https://cobalt.io/piwik-open-source-analytics)
- [Plone](mailto:security@plone.org)
- [Pocket](mailto:security@getpocket.com)
- [Poloniex](https://cobalt.io/poloniex)
- [Postmark](https://wildbit.wufoo.com/forms/wildbit-security-response)
- [Prezi](mailto:security-bug-bounty@prezi.com)
- [Projectplace](https://hackerone.com/projectplace)
- [PullReview](mailto:security@pullreview.com)
- [Puppet labs](mailto:security@puppetlabs.com)
- [PureVPN](https://bugcrowd.com/purevpn)
- [Python](mailto:security@python.org)
- [QIWI](https://hackerone.com/qiwi)
- [Quadriga CX](https://cobalt.io/quadriga-cx)
- [QuickBT](https://cobalt.io/quickbt)
- [Quora](https://hackerone.com/quora)
- [Rackspace](mailto:security@rackspace.com)
- [Rdbhost_service](https://cobalt.io/rdbhost-service)
- [Red Hat](mailto:site-security@redhat.com)
- [Reddit](mailto:security@reddit.com)
- [Relaso](mailto:security@relaso.com)
- [RelateIQ](mailto:security@relateiq.com)
- [Release Wire](http://www.releasewire.com/about/contact)
- [Respondly](https://hackerone.com/respondly)
- [Revive Adserver](https://hackerone.com/revive_adserver)
- [Ribose](https://www.ribose.com/feedbacks/security)
- [Ripio](https://cobalt.io/ripio)
- [Ripple](mailto:bugs@ripple.com)
- [Riskalyze](mailto:security@riskalyze.com)
- [Romit](https://hackerone.com/romit)
- [Ruby](mailto:security@ruby-lang.org)
- [Ruby on Rails](https://hackerone.com/rails)
- [Salesforce](mailto:security@salesforce.com)
- [Samsung TV](https://samsungtvbounty.com/ReportBug.aspx)
- [Sandbox Escape](https://hackerone.com/sandbox)
- [SAP](mailto:secure@sap.com)
- [Schuberg Philis](mailto:abuse@schubergphilis.com)
- [Scorpion Software](mailto:security@scorpionsoft.com)
- [Secret](https://hackerone.com/secret)
- [Secure Works](mailto:security@secureworks.com)
- [Sellfy](http://docs.sellfy.com/contact)
- [Sentiance](https://go.intigriti.com/sentiance)
- [ServiceRocket](https://bugcrowd.com/servicerocket)
- [ShareLaTeX](mailto:team@sharelatex.com)
- [Sherpany](https://cobalt.io/sherpany)
- [Shopify](https://hackerone.com/shopify)
- [Sifter](mailto:security@sifterapp.com?subject=%27Security%20Vulnerability%20Report%27)
- [Silent Circle](https://bugcrowd.com/silentcircle)
- [Simple](https://bugcrowd.com/simple)
- [SiteGround](mailto:responsible-disclosure@siteground.com)
- [Skoodat](mailto:security@skoodat.com)
- [Skrill](https://cobalt.io/skrill)
- [Skyscanner](https://bugcrowd.com/skyscanner)
- [Slack](https://hackerone.com/slack)
- [Snapchat](https://hackerone.com/snapchat)
- [Snappy](mailto:security@userscape.com)
- [Sonatype](mailto:security@sonatype.com)
- [Sony](https://secure.sony.net/form)
- [SoundCloud](https://scsecurity.freshdesk.com/support/tickets/new)
- [Spaargids](https://go.intigriti.com/spaargids)
- [SpectroCoin](https://cobalt.io/spectrocoin)
- [Spendbitcoins](https://cobalt.io/spendbitcoins)
- [SplashID](https://bugcrowd.com/splashid)
- [Splitwise](mailto:security@splitwise.com)
- [Spotify](mailto:security@spotify.com)
- [Sprout Social](mailto:security@sproutsocial.com)
- [Square](https://hackerone.com/square)
- [Square Open Source](https://hackerone.com/square-open-source)
- [StatusPage](https://bugcrowd.com/sunrise)
- [StopTheHacker](https://hackerone.com/stopthehacker)
- [Student Assessment System](https://go.intigriti.com/printscan)
- [Studio 100](https://go.intigriti.com/studio100)
- [Subledger](https://cobalt.io/subledger)
- [Subrosa](https://cobalt.io/subrosa)
- [Sucuri](https://hackerone.com/sucuri)
- [Suivo](https://go.intigriti.com/suivoweb)
- [Symantec](mailto:secure@symantec.com)
- [Taptalk](https://hackerone.com/taptalk)
- [Tarsnap](mailto:cperciva@tarsnap.com)
- [TeamUnify](mailto:security@teamunify.com)
- [Tele2](mailto:beveiligingsmeldpunt@tele2.com)
- [Telekom](mailto:cert@telekom.de?subject=bug_bounty)
- [Telenet](https://go.intigriti.com/telenet)
- [Test-Aankoop](https://go.intigriti.com/testaankoop)
- [The Internet](https://hackerone.com/internet)
- [The Mastercoin Foundation](https://cobalt.io/the-mastercoin-foundation)
- [ThisData](https://hackerone.com/thisdata)
- [TimeTrex](https://cobalt.io/timetrex)
- [ToyTalk](https://hackerone.com/toytalk)
- [Trello](https://hackerone.com/trello)
- [Tuenti](http://corporate.tuenti.com/en/contact/security)
- [Tweakers](https://go.intigriti.com/tweakers)
- [Twilio](https://bugcrowd.com/twilio)
- [Twitch](mailto:security@twitch.tv)
- [Twitter](https://hackerone.com/twitter)
- [Uber](mailto:security-abuse@uber.com)
- [Ubiquiti Networks](https://hackerone.com/ubnt)
- [Unitag](mailto:security@unitag.io)
- [Urban Dictionary](https://hackerone.com/urbandictionary)
- [Uzbey](https://hackerone.com/uzbey)
- [Valve Software](mailto:security@valvesoftware.com)
- [VeChainThor](https://hackenproof.com/vechain/vechainthor)
- [VeChainThor Wallet](https://hackenproof.com/vechain/vechainthor-wallet)
- [VCE](mailto:security-alerts@vce.com)
- [Venmo](mailto:security@venmo.com)
- [Version Cake](https://hackerone.com/versioncake)
- [Viadeo](mailto:security@viadeo.com)
- [Vimeo](https://hackerone.com/vimeo)
- [VK.com](https://hackerone.com/vkcom)
- [Volusion](https://bugcrowd.com/volusion)
- [VPNSox](https://cobalt.io/vpnsox)
- [vulners.com](https://hackerone.com/vulnerscom)
- [Vultr](https://www.vultr.com/bug-bounty/)
- [Webconverger](mailto:security@webconverger.com)
- [Websecurify](http://campaigns.websecurify.com/money-for-bugs/#contact)
- [Weebly](https://cobalt.io/weebly)
- [WePay](https://hackerone.com/wepay)
- [Whisper](https://hackerone.com/whisper)
- [WHMCS](https://bugcrowd.com/whmcs)
- [Windthorst ISD](http://www.windthorstisd.net/BugReport.cfm)
- [withinsecurity](https://hackerone.com/withinsecurity)
- [WizeHive](mailto:security@wizehive.com)
- [Woorank](https://go.intigriti.com/woorank)
- [WordPoints](https://hackerone.com/wordpoints)
- [Wordware](https://cobalt.io/wordware)
- [WP API](https://hackerone.com/wp-api)
- [Xen Project](mailto:security@xenproject.org)
- [Xmarks](mailto:security@lastpass.com)
- [Yahoo](https://hackerone.com/yahoo)
- [Yandex](https://yandex.com/bugbounty/report)
- [Yanomo](mailto:support@yanomo.com)
- [Yesware](mailto:security@yesware.com)
- [Zapier](mailto:security@zapier.com)
- [Zaption](https://hackerone.com/zaption)
- [ZenCash](mailto:security@zencash.com)
- [Zendesk](https://hackerone.com/zendesk)
- [Zetetic](mailto:support@zetetic.net)
- [Ziggo](mailto:security@ziggo.nl)
- [Zimbra](mailto:security@zimbra.com)
- [Zoho](https://bugbounty.zoho.com/bb/info) 
- [Zomato](https://hackerone.com/zomato)
- [Zopim](https://hackerone.com/zopim)
- [Zynga](mailto:whitehat@zynga.com)

### Online Readings
<ul>
  <li><a ref="https://bugbountytuts.files.wordpress.com/2018/02/dirty-recon.pdf">Recon Like A Boss</a></li>
  <li>https://whitton.io/articles/bug-bounties-101-getting-started/</li>
  <li><a href="https://github.com/jhaddix/tbhm">The Bug Hunters Methodology</a></li>
  <li><a href="https://github.com/EdOverflow/bugbounty-cheatsheet">Bug Bounty Cheatsheet</a></li>
  <li><a href="https://github.com/ngalongc/bug-bounty-reference/">Bug Bounty Reference</a></li>
  <li><a href="https://github.com/bugcrowd/vulnerability-rating-taxonomy">Bugcrowd Vulnerability Rating Taxonomy (VRT)</a></li>
  <li><a href="https://hackerone.com/hacktivity">Hackerone Hacktivity</a></li>
  <li>https://www.hackerone.com/blog/What-To-Do-When-You-Are-Stuck-Hacking</li>
  <li>https://www.quora.com/How-does-one-become-a-bug-bounty-hunter/answer/Jobert-Abma</li>
  <li>https://www.quora.com/How-much-time-did-you-take-from-completely-beginning-hacking-to-your-first-success-or-bug-bounty/answer/Jobert-Abma</li>
  <li>https://www.quora.com/How-do-bug-bounty-hunters-find-bugs/answer/Jobert-Abma</li>
  <li>https://www.quora.com/How-much-can-I-make-in-my-first-year-as-a-bug-bounty-hunter</li>
  <li>https://blog.detectify.com/2019/05/03/meet-the-hacker-inti-de-ceukelaire-while-everyone-is-looking-for-xss-i-am-just-reading-the-docs</li>
  <li>http://blog.oath.ninja/basic-bug-bounty-faq</li>
  <li>https://twitter.com/spaceraccoonsec</li>
</ul>
 
 ### Online Videos
 <ul>
  <li><a href="https://sites.google.com/site/bughunteruniversity/">Google Bughunter University</a></li>
  <li>https://www.hacksplaining.com/lessons</li>
  <li>https://www.udemy.com/android-application-penetration-testing-ethical-hacking/</li>
  <li>https://www.youtube.com/user/Hak5Darren/playlists</li>
  <li>https://www.youtube.com/user/DEFCONConference/videos</li>
  <li>https://www.youtube.com/user/JackkTutorials/videos</li>
  <li>https://www.youtube.com/watch?v=mQjTgDuLsp4</li>
  <li>https://www.youtube.com/watch?v=KDo68Laayh8</li>
  <li>https://www.youtube.com/watch?v=XoYF-euS-zs</li>
  <li><a href="https://www.youtube.com/watch?v=Q2WK5LpDbxw">Finding Bugs with Burp Plugins & Bug Bounty 101</a></li>
 </ul>

### Forums / Blogs
<ul>
  <li>https://www.bugcrowd.com/about/blog/</li>
  <li>https://www.reddit.com/r/netsec</li>
  <li>https://www.reddit.com/r/websecurity/</li>
</ul>

### Other Aggregated Resources
<ul>
  <li>https://www.hackerone.com/blog/resources-for-new-hackers</li>
  <li>https://www.peerlyst.com/posts/the-everything-bug-bounty-wiki-peerlyst?trk=company_page_posts_panel</li>
  <li>https://github.com/onlurking/awesome-infosec</li>
  <li>https://forum.bugcrowd.com/t/researcher-resources-tutorials/370</li>
  <li>https://forum.bugcrowd.com/t/researcher-resources-tools/167</li>
  <li>https://forum.bugcrowd.com/t/how-do-you-approach-a-target/293</li>
  <li>http://www.amanhardikar.com/mindmaps/Practice.html</li>
  <li>https://github.com/djadmin/awesome-bug-bounty</li>
</ul>

# Thank You ❤

[![image](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/NandanLohitaksh) [![](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/lohitakshnandan) [![](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lohitakshnandan)

</div>

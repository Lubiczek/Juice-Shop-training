\# Password cracking + price manipulation



As now i am in hold of knowledge that sql injection is working i can see what type of token other accounts have. I look for every email i could find in reviews on the site. For example.





!\[Screenshot\_of\_jim's\_review](./images/jim\_rev.png)



jim@juice-sh.op is the next email i could find



I used the same sql injection trick as before to get inside his account



!\[Screenshot\_of\_sql\_trick](./images/jim\_sql.png)



As i am now capable of looking for information about Jim i am scrolling through his account for something interesting. Unfortunately this time only thing i found are normal reviews under products. Now i tried to see more information about stan's account. In order to do that i copied his token and decode it from base64 using CyberChef. Here are results.



!\[Info\_about\_jim's\_acc](./images/Info\_about\_Jim\_acc.png)



Info i found: Jim's ID - 2, hash\_of\_password - e541ca7ecf72b8d1286474fc613e5e45 



Thats a good info. Now i tried to crack Jim's password. With usage of hashes.com i am able to do it without a problem. 



!\[Screenshot\_of\_Jim's\_password](./images/jim\_pass\_id\_2.png)



Jim's password is ncc-1701



Now i was looking for other interesting accounts and passwords that was connected to them. 

I Stumbled upon several accounts that some couldnt crack so easily with hashes.com or even hashcat. Examples of password i found:



!\[Screenshot\_of\_bender](./images/benders\_pass\_id\_3.png)



!\[Screenshot\_of\_mcc](./images/mc\_safe\_search\_pass\_id\_8.png)



!\[Screenshot\_of\_admin\_pass\_id\_1](./images/admin\_pass\_id\_1.png)



\# Price manipulation



One of the core function of a site is "buying products". The prices varies a lot. From 0.99 to 9999 currency of OWASP Juice Shop. However one of the account have the ability to change all of the prices.



!\[Screenshot\_of\_acc\_acc](./images/acc\_acc.png)



I stumbled around accountant account. After using sql injection i saw that there is "Accounting" function connected to the profile. If we go inside we can see that the user now have ability to change every price in the shop.



!\[Screenshot\_of\_acc\_func](./images/acc\_func.png)



Now i changed everything so it costs 0 value of currency.



!\[Screenshot\_of\_value\_drop](./images/value\_drop.png)



We can buy everything for 0 value of currency.


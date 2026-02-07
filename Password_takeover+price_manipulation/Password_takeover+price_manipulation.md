# Password cracking + price manipulation


As now i am in hold of knowledge that sql injection is working i can see what type of token other accounts have. I look for every email i could find in reviews on the site. For example.


![Screenshot_of_jim's_review](./images/jim_rev.png)



jim@juice-sh.op is the next email i could find



I used the same sql injection trick as before to get inside his account



![Screenshot_of_sql_trick](./images/jim_sql.png)



As i am now capable of looking for information about Jim i am scrolling through his account for something interesting. Unfortunately this time only thing i found are normal reviews under products. Now i tried to see more information about stan's account. In order to do that i copied his token and decode it from base64 using CyberChef. Here are results.



![Info_about_jim's_acc](./images/Info_about_Jim_acc.png)



Info i found: Jim's ID - 2, hash_of_password - e541ca7ecf72b8d1286474fc613e5e45 



Thats a good info. Now i tried to crack Jim's password. With usage of hashes.com i am able to do it without a problem. 



![Screenshot_of_Jim's_password](./images/jim_pass_id_2.png)



Jim's password is ncc-1701



Now i was looking for other interesting accounts and passwords that was connected to them. 

I Stumbled upon several accounts that some couldnt crack so easily with hashes.com or even hashcat. Examples of password i found:



![Screenshot_of_bender](./images/benders_pass_id_3.png)



![Screenshot_of_mcc](./images/mc_safe_search_pass_id_8.png)



![Screenshot_of_admin_pass_id_1](./images/admin_pass_id_1.png)



# Price manipulation



One of the core function of a site is "buying products". The prices varies a lot. From 0.99 to 9999 currency of OWASP Juice Shop. However one of the account have the ability to change all of the prices.



![Screenshot_of_acc_acc](./images/acc_acc.png)



I stumbled around accountant account. After using sql injection i saw that there is "Accounting" function connected to the profile. If we go inside we can see that the user now have ability to change every price in the shop.



![Screenshot_of_acc_func](./images/acc_func.png)


Now i changed everything so it costs 0 value of currency.

![Screenshot_of_value_drop](./images/value_drop.png)

We can buy everything for 0 value of currency.


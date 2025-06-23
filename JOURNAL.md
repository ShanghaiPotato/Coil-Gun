Journal.md
Tital: Coilgun
Author: Ziqi Guan
Desciption: The aim is to create a multi-stage coilgun with decent acceleration and speed. The desired range is 30-40 feet.
Created at: 6/17/2024

June 17th - Log 1
Started at 9:00 pm
Took a 45 min breka from 10:05-10:50 pm
Ended at 12:00 am (Midnight)
Session Time: 2 hrs 15 mins
Total Time: 2 hrs 15 mins

Premise: (NEED TO UPDATE SOME OTHER TIME)

Mainly did research and concept exploration. I have already done a lot of research, but a bit more wouldn't hurt, especially since the pcb for this will be decently complicated considering the sensors have to send signals with little delay.

Videos Watched for guidance and inspiration:
    https://www.youtube.com/watch?v=PMU9TQUDhow
    https://youtu.be/id90kjYh-Qw?si=KB8jq6l4MKs8E-xA     Electronoob
    https://www.youtube.com/watch?v=rotrRg4ZUpk
    https://www.youtube.com/watch?v=QTDcFxTq1Fw           Hacksmith
    https://youtu.be/AwRJsze_9m4?si=WbC6bxTEcL72BCi7      Engineering Mindset: Mosfets (Good guide to how mosfets work and why they are used over transisters)
    https://youtu.be/gADIb1Xw8PE?si=Rg8etwbdkOXKYFJh      Video all about IR and how to send and recieve
    https://youtu.be/X4EUwTwZ110?si=Mn7Il1-l6g907hk5      Engineering Mindset: Capacitors (Video all about Capacitors and how they work)



Question I have/Need to research:
    1.Instead of a detector on the side of the barrel, would it be possible to measure speed and distance with a single light sensor at the end of the barrel.

    Update: After doing some research and searching, the best way forward is to just have sensors on the side. While a single sensor would easily make everything easier, it also presents a lot of challenges that I might not be able to troubleshoot. Even though I want to use a method different than what everyone else uses, there isn't really a cheaper or more efficient method than IR sensors on the side of the barrel. 

    2.Should I use a low voltage system (Safer, easier, cheaper, weaker, and more accessable) or a high volatage capaciter system (Dangerous, harder, potentially more expensive, stronger, less accessable, bulkier, and more timing heavy).

    Update: After multiple considerations, using high voltage capacitors will probably work best. This is because their higher voltage means more current in the short amount of time. Of course that means that this might increase the price and caution should be taken when handling the parts. 

Key Things to note:
1.
    A: Inductive Loads take time to reach full current
    B: Resistive Loads reach full current almost immedietly and doesn't lag behind the voltage that much.

    That means the inductive loads we are using must be activated before the projectile enters the magnetic field for the electromagnet to reach its full stregnth. 
2.
    Most people are using high voltage capacitors. The pros and cons are still something I need to look at, but it seems like the better option for more speed. 
    I also believe that 3-4 stages will be more than enough given the many features I want to add that I have to figure out. 
3.
    Multiple systems need to be integrated together well, also high voltage capacitors seem like the best option. Main thing though is calculating the speed of the projectile and acceleration on the coilgun with speed as any latency could mean that coils get activated too late. 

Plans:
    The coilgun I wish to design should be completely mobile and be able to be held unlike most designs on the internet. Not only are most clunky with exposed wiring, I believe that it leads to inefficiency. While Electronoobs design of modularity was good, the amount of components needed in my opinion was not great. It should also have features such as a reload system (probably only 5 rounds or so), capacitor reading system (to indicate whether or not the capacitors are at full charge), and settings to disable stages (to reduce speed and acceleration). 

Photos: Will add more later because I don't want to just upload youtube screenshots right now. 
![alt text](image.png)


June 18th - Log 2
Started at 8:45 pm
Ended at 9:20 pm
Session Time: 35 mins
Total Time: 2 hrs 50 mins

Main Goals: 
1:
    Began a concept CAD on OnShape for the coilgun, while the PCB isn't designed yet and many things can change, a rough idea of what I'm working with helps a lot, especially with spacing. 
2: 
    Began working in kiCAD to design the PCB, although this is probably not going to be achievable as I have to design the circuit still, so more of a design circuit thing.
3:
    More of a task 2 part 2, but research more into the electrical componenets, if there are any ways to simplify the design, it would be great as the entire system has to be handheld 

Videos watched:
https://youtu.be/hNRzK9SiqQA?si=KOMdYGKCFp1c2ixh       Video about thyristors (potential option apart from a MOSFET)
https://youtu.be/vtoWxGVx5kA?si=DG7lvUVK3ucVBTBL       Electronoobs follow up video to his first coilgun video

Began to desgin coilgun PCB with a rough sketch.


June 19th - Log 3
Started at 8:50 pm
Ended at 10:40 pm
Session Time: 1 hr 50 mins
Total Time: 4 hrs 40 mins

Was busy yesterday so I couldn't do everything that I could do. Today I'm going to just focus fire the PCB design and put good thought into it as it will determine how the coilgun will look. 

Spent most of the time going into various rabbit holes of different electrical parts. Could have been shorter but it's fine. 

Very rough photo of the circuit design. I'll have to refine it later and do some more research into all the pins on the teensy. 
  ![alt text](image-1.png)

June 21th - Log 4
Started at 11:30 am
Took a 1 hr break to eat and walk dog
Ended at 4:00 pm
Session Time: 1 hr 50 mins
Total Time: 4 hrs 40 mins

Main things to do today:
1.
    Begin the BOM (even if it is a rough draft) to figure out the cost and finding the parts. 
2.
    Finish up researching each part of the components such as the wire size, spacing, capacitor capacitance, and safety features.
3.
    Begin to put all of that in the journal for quicker reference and begin to create a tutorial/explanation document. 
4.
    If possible finish up the schematics and start putting it on kiCAD.

Quick calculations that are important to the coilgun:
1.
    The projectile should leave the barrel after .0075 seconds or 7.5 miliseconds (like playing with a 7.5 ping), so that means we need devices that can respond in microseconds (like the teensy) 1 microsecond = 1/1,000,000 second.
2.
    To handle 100 amps of pulse current, I plan on using 14 guage wire as it should hold (and as long as I don't spam the coilgun). 
3.
    For each of the coil stages, I plan on 2 inch long coils with an inner diameter of .3 inches and an outer diameter of 2 inches. This does mean though that the coils will probably have to be handwoven.
Potential links for the BOM:
https://www.aliexpress.us/item/3256805844530735.html?src=google&pdp_npi=4%40dis%21USD%217.26%217.26%21%21%21%21%21%40%2112000035401398484%21ppc%21%21%21&src=google&albch=shopping&acnt=708-803-3821&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&gclsrc=aw.ds&albagn=888888&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=en3256805844530735&ds_e_product_merchant_id=780602513&ds_e_product_country=US&ds_e_product_language=en&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=19678427463&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=19686402437&gbraid=0AAAAAD6I-hGHNDpM0iIcZmqwdoZnpor_m&gclid=Cj0KCQjwsNnCBhDRARIsAEzia4De12C6hIc_aGuUkQ1mCi7W5En3swpTUHt-JGkklspzJJdDDO49Zf0aApWQEALw_wcB&gatewayAdapt=glo2usa
https://www.aliexpress.us/item/3256803137393104.html?spm=a2g0o.productlist.main.4.344d5d4fKtE4ho&aem_p4p_detail=2025062111382214154563376233880004464488&algo_pvid=37ba1ed5-cdf7-4fc9-b228-c2198b3a817d&algo_exp_id=37ba1ed5-cdf7-4fc9-b228-c2198b3a817d-3&pdp_ext_f=%7B%22order%22%3A%22815%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%213.88%213.54%21%21%213.88%213.54%21%402103245417505311026777131e1c62%2112000025211444658%21sea%21US%210%21ABX&curPageLogUid=YBKzzHsToF6V&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=2025062111382214154563376233880004464488_1
https://www.aliexpress.us/item/3256808777064165.html?src=google&pdp_npi=4%40dis%21USD%2117.92%215.86%21%21%21%21%21%40%2112000047399054015%21ppc%21%21%21&src=google&albch=shopping&acnt=708-803-3821&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&gclsrc=aw.ds&albagn=888888&ds_e_adid=&ds_e_matchtype=&ds_e_device=c&ds_e_network=x&ds_e_product_group_id=&ds_e_product_id=en3256808777064165&ds_e_product_merchant_id=5582814949&ds_e_product_country=US&ds_e_product_language=en&ds_e_product_channel=online&ds_e_product_store_id=&ds_url_v=2&albcp=19678427463&albag=&isSmbAutoCall=false&needSmbHouyi=false&gad_source=1&gad_campaignid=19686402437&gbraid=0AAAAAD6I-hGHNDpM0iIcZmqwdoZnpor_m&gclid=Cj0KCQjwsNnCBhDRARIsAEzia4AVE59NkNSb3vcKgFLixu86Wqfh9rRQSVuMHJ4rNFdj-6Ds6YR5oTsaAorGEALw_wcB&gatewayAdapt=glo2usa - 12v 3Ah Lipo Battery
https://www.mightymaxbattery.com/shop/12v-sla-batteries/ml5-12-12-volt-5-ah-sla-battery/ - 12v 5Ah SLA Battery (Probably better option)
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
  ![alt text](RoughSchematicSketch.png)

June 21th - Log 4
Started at 11:30 am
Took a 1 hr break to eat and walk dog
Ended at 4:00 pm
Session Time: 3 hr 30 mins
Total Time: 8 hrs 10 mins

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

June 22th - Log 5
Started at 9:20 pm
Ended at 12:00 am (Midnight)
Session Time: 2 hrs 40 mins
Total Time: 10 hrs 50 mins

List of things I need to do because I haven't been that organized the last couple of days. A lot of the things I put in this log are quick notes about things I notice and need to keep track of, but now I need to actually create a list of everything I need to do to make sure I finish it. 

List of things:
1.
    Finish researching the optimal voltage and current flow for the coilgun considering cost, wear, safety, and complexity. 
2.
    Design schematics for all the electrical components - On/off switch, boost converty, inductors for the coils, voltage detector, microcontroller wiring. 
3.
    Design the physical case that the coilgun will be in. 

Calculations for some things:
1. Optimal voltage and current flow - 
    I contemplated over dropping the voltage down to 300v instead of 450v because there are more parts that can handle 300v, but lower voltage means lower current rise which means that it takes longer for the coils to reach their full magnetc potential. If I'm using a 450v capacitor with 1000 microfarads (which is pretty highfor microfarads) and the equation for capacitors is Capacitance (farads) = Electrons (coulombs) / Voltage, which means that the amount of coulombs is just the capacitance multiplied by the voltage. With that number you can roughly calculate the amperage by dividing the coulombs by the amount of time the coil will be on. This part gets tricky as an inductor load's current rises slower and is more of a curve than being instantaneous. I'm going to admit it, using chatGPT to crunch the numbers was a lot more efficient. Crunching the numbers, using a 450V 500µF capacitor with a 2in long 2in OD .3in ID coil with 14AWG copper wire, the peak current is around 500AMPs (although will be much lower) and reaches peak current at around .5ms or 500 microseconds (half a ping). This is perfect because the iron rod should exit the barrel after roughly 7ms or 7000 microseconds, so I have plenty of time.
        Summary: Using a 450V 500µF Capacitor with a 2in long, 2in OD, .3in ID 14AWG copper coil will result in a peak current of 500AMPs after .5 miliseconds. 

2. Time to charge the capacitors -
    Preferably the time to charge the capacitors should hopefully be under 5 seconds (as thats how fast you should be able to reload this bolt-action coilgun). The equation should be simple, take the amperage of the DC-DC boost converter and the coulomb count and number of capacitors and do some basic math. Assuming a 450V 500µF capacitor, the coulombs should be .225 coulombs. Multiply that by 4 capacitors and you get .9 coulombs. That means .9amps should charge all the capacitors to full charge in one second. There is one caveat that some current will be drained for the LED voltage detector (more on that later). The next important thing to consider is how much current is flowing through the DC-DC boost converter. 
    
    After looking at the best DC-DC boost converter I could find (Link at the end of this log), it says that it can charge a 450V 1000µF capcitor in 5 seconds, which is dissapointing because running the math thats .45 coulombs in 5 seconds, which means it will take 10 seconds to charge the four capcitors. It makes sense though, 450V is a lot, but it also means the DC-DC Boost converter will draw a crap ton of current. The manufacturer reccomends 7AMPs continously. The Mighty Max battery I plan on using can handle that for up to 20 mins so that aspect should be fine. Of course I'm not considering the rest of the elctronics, but for the most part their current draw will be in miliamps. 
        Summary: The time to charge 4 capacitors will be roughly 10 seconds, drawing 7AMPs continously from the battery. 

3. Voltage LED Readers - 
    To indicate when the capacitors are fully charged, I plan on adding zener diodes and LEDs in parallel from the coil to measure the voltage. The zener diodes will essentially "reduce" the voltage and current enough for an LED to safely light up when enough voltage is applied. The main issues are current leaking (as the DC-DC boost converter charges really slow), zener diodes potentially failing at high voltage, and flyback from the coil. The current leaking should be minimal though (as only 20mA are going through the wire to power the LED at most), and the zener diodes should be fine as long as multiple are used. As for the flyback, some diodes rated for high voltages should work just fine. 

4. Flyback Protection - 
    Inductors have voltage spikes when abruptly turned off (article at the end of the log) and pose a danger to the MOSFET. There is also the issue that if we use a flyback diode, then current will continue to flow through the inductor after the iron projectile has passed through, leading to the projectile experiencing a backward force. A 20A 1000V Diode can handle this as the firing frequency will be low, but the continuous magnetic field is a concern. It defeats the purpose of a MOSFET shutting down the coil part of the way through the capacitor discharge. An option is to add a resistor along the flyback diodes path to reduce current, the issue becomes that there will be a higher voltage spike to make up for the increased resistance. For safety and preservation of electrical componenets, I'm going to just let the magnetic field collapse on its own. One thing to note though is that the field rapidly degrades, chatGPT made a rough chart, and 500 microseconds to collapse the field isn't too bad. 
    ![alt text](MagneticFieldPersistance.png)

DC-DC Boost Converter - https://www.aliexpress.us/item/3256809063920342.html?spm=a2g0o.productlist.main.13.6d02248cg9pQrR&algo_pvid=12e0f6be-be09-4bd7-8c7c-19c1ab4e774f&algo_exp_id=12e0f6be-be09-4bd7-8c7c-19c1ab4e774f-12&pdp_ext_f=%7B%22order%22%3A%22-1%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%2128.24%2118.64%21%21%2128.24%2118.64%21%40210337c117506447569233788e2c8d%2112000048474873422%21sea%21US%210%21ABX&curPageLogUid=wZoh731edbtN&utparam-url=scene%3Asearch%7Cquery_from%3A
100V Zener Diode - https://www.mouser.com/ProductDetail/Vishay-General-Semiconductor/Z4KE100A-E3-73?qs=D6r9GjgEnNO6SbLZQJ%2Fl6A%3D%3D
20A 1000V Diode - https://www.aliexpress.us/item/3256808009577580.html?spm=a2g0o.productlist.main.8.3cae14d5bMksTu&aem_p4p_detail=202506222030244762503293716800006192091&algo_pvid=5cc7d710-6d38-4990-8bdc-69aafab4f526&algo_exp_id=5cc7d710-6d38-4990-8bdc-69aafab4f526-7&pdp_ext_f=%7B%22order%22%3A%228%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.41%212.21%21%21%2117.25%2115.82%21%4021030ea417506494247553981ee0d2%2112000044199180347%21sea%21US%210%21ABX&curPageLogUid=8llMqoc7OgXd&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202506222030244762503293716800006192091_2

Article explaining Flyabck Diodes and their importance - https://digilent.com/reference/learn/fundamentals/electronic-components/flyback-diodes/start?srsltid=AfmBOoogx0JYhg6oxVeq-Q9626j1oq6hILmMAzFk_kgQ6rXLRWM8fnhP
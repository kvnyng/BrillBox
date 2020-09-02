# BrillBox

## Check out my pitch video!
[Video:] (https://www.youtube.com/watch?v=0VwampxgdxY) https://www.youtube.com/watch?v=0VwampxgdxY
## Introduction
With the shortage of PPE in hospitals and masks surging in price on online delivery sites, the public has resorted to taking their own initiative to protect themselves. This initiative has primarily become prevalent with anyone that has 3-D printers or sewing equipment. With organizations such as Helpful Engineering creating and certifying 3-D printed mask designs, they help set the standard of safety in the D.I.Y PPE community. Yet, how does the public know if their masks are still safe after a certain amount of uses? Our mouths are essentially a vacuum, sucking up surrounding particulates. When an N-95 mask is worn, these particulates get sucked towards our faces only to be stopped by the mask. Over time, germs, dirt, and viruses will populate themselves onto the surface, turning it into a health hazard to anyone that touches it. 

This same question can also apply to essential workers’ clothing, as these employees are at work for most - if not all - days of the week. During their long shifts, their clothes will not only pick up grime like everyone else's, but also bacteria and viruses that are floating around in the air or multiplying on countertops and furniture. 
Even with consistent wash-and-dry techniques, the virus may still be present on clothes, homemade masks, and other fabrics that humans have frequent, skin-based contact with. Thus, there is a need for the general public to have access to a way to clean their PPE from dirt and grime but also from germs and viruses. This is where BrillBox comes in. 

## Purpose & Motivation
With the surge of COVID-19, there has also been a huge spike in demand for PPE, most notably masks. This increase in demand quickly left pharmacy shelves bare of surgical and N-95 masks. To solve this, mask producing companies such as 3M and Honeywell have sought it to increase their production of PPE. This tactic, although simple in nature, will do very little to stifle the demand of masks. Instead, the solution to the lack of PPE is finding a way to constantly reuse it.

Likewise, in respect to frontline workers, constant washing and steaming of clothes is not efficient nor convenient. As for at-home mask makers, the materials used in a mask may typically derive from materials such as cloths and paper-based filters. It is immediately obvious that these materials will degrade after continuous washing, prompting the user to require more masks and more PPE. 

These issues can be easily solved by using a sterilizer, which can destroy germs and viruses that may be present on the surface. Although this technology is widely used in labs it costs far too much for the average user to buy (a lab sterilizer hovers around $7000). Besides this, currently, there is no commercially available sterilizer meant to clean PPE and masks. 

With all this said, it is immediately obvious that to extend PPE supply, save hospital workers time, and find a way to reuse non-washable filters, we need a cheap, user-friendly sterilizer. 

## How BrillBox Works
It is a well-known fact in biology that UV radiation breaks down DNA and RNA, eradicating germs, and viruses. Knowing this, all that is needed to sanitize PPE is a concentrated amount of UV for 15 minutes. 

To achieve this, Brillbox uses off-the-shelf germicidal bulbs operating in the 264nm range. This wavelength has been tested to be the most efficient at destroying RNA. From there, all that is needed is a special control circuit that will be able to turn the bulbs on and off. This controller comprises of an Arduino Nano, a voltage regulator, a resistive ballast, and a relay, among other miscellaneous parts. Likewise, the control circuit also interfaces with the UI of the box, which is simply two buttons, a buzzer, and an LCD display.  

The schematic for the entire project is linked in the gallery (above)

## Cost
Due to the simplicity of the design, the entire box costs about $12 to produce and is able to sanitize up to 160,000 masks before needing to replace the germicidal bulbs. 

**The cost of each individual component is as follows:**

Arduino Nano - **$1.70**

Buzzer - **12¢**

LCD Display - **$2**

Buttons (2) - **50¢**

Germicidal Bulbs (2) - **$8**

Cardboard Box - **Free**

Aluminum Foil - **30¢**

Relay - **50¢**

Reed Switch + Small Magnet -**8¢**

**Total: $11.20**

**Note:** The 160,000 comes from the following calculations:
The bulbs last for an average of 50,000 hours or 300,000 minutes.
Each mask requires at most, 15 minutes to sterilize. 
8 surgical masks can be sterilized at the same time. 
**(300,000/15)*8 =160,000**

## A Note on Safety
Brillbox is designed with safety in mind. 

Using UV germicidal bulbs, it is obvious that users may first feel apprehensive of the product. This apprehension is understandable but the Brillbox team has done many things to increase user safety. 

Brillbox uses 264 nm UV waves, a subset of the UV-C range. Although UV is able to cause skin cancer, the [UV-C range is not the wavelength associated with skin cancer] (https://www.cancer.org/cancer/cancer-causes/radiation-exposure/uv-radiation.html) (UV-A to UV-B). Likewise, the bulbs used in Brillbox are low power (3 watts), a small fraction compared to the [175 watts that reach the Earth from the Sun] (http://www.shespeaksscience.com/solar-cells/#:~:text=If%20we%20account%20for%20light,175%20Watts%20per%20square%20metre). This means that, in direct contact with the skin, the UV-C will have little affect for short periods of time. 

It is also important to point out that UV does not have the same properties as Alpha or Gamma particles. UV waves can be reflected by certain materials, most notably water, glass, and aluminum. To contain the radiation, the inside of the box is lined with two layers of aluminum foil, helping to reflect the UV rays towards the masks. This increases both the efficiency of the box and as well as keeping users safe from potential contact. 

Ozone may also be a concern as many UV sanitation devices produce the dangerous gas to increase sanitation efficiency. Although this would benefit Brillbox, ozone, when inhaled, can trigger [asthma attacks, chest pain, coughing, and other respiratory complications] (https://www.epa.gov/indoor-air-quality-iaq/ozone-generators-are-sold-air-cleaners#:~:text=When%20inhaled%2C%20ozone%20can%20damage,body%20to%20fight%20respiratory%20infections). Thus, the Brillbox team has opted to use ozone-free bulbs to users from potential ingestion. 
Last but not least, if the Brillbox lid is ever opened during operation, the control circuit will instantly turn off the UV bulb. This is to ensure that the user will never come in contact with the UV present in the device. 

Overall, the team at Brillbox has done extensive research on UV sanitization. The team has taken all the necessary steps to prevent any complications from happening, protecting the user, loved ones, pets, and anyone else that uses Brillbox. 

## Difficulties and Challenges Faced
There were many challenges that the Brillbox team had to overcome to arrive at where we are today. For instance, our team went over 2 different ideas to get to the idea of sanitizing PPE. 

Our first idea was to utilize small particles to measure the efficiency of a mask, which evolved to using a laser that has the same wavelength as the diameter of COVID-19 (60-140nm). The basic principle is to measure how much light is able to pass through the mask in question. From there, we are able to calculate how small the holes are in the mask and how effective it would be in the medical setting. This project fell through because the wavelength needed (60-140nm) is in the high end of the UV range, and in a laser form, would pose a health risk to anyone that is not an optics professional. 

Our second idea was to make an enclosed mask, kinda like a scuba mask, that will isolate the user from the outside environment. It would use the hot side of a Peltier module to kill incoming bacteria and viruses, and on the cold side, would generate a climate-controlled environment. This would essentially mean the user would have A/C in his mask, keeping the user cool throughout the day. The main application for this mask would be hospital workers who have to operate on patients for 8+ hours a day. Keeping cool is a necessity for them, however, this idea fell through simply because Peltier modules are unable to reach the 100° needed to destroy proteins at an affordable price point. 

Besides going through multiple ideas trying to get the UV bulbs to work was extremely tiresome and laborious. Bought off of Amazon, the UV bulbs lack any substantial documentation. Therefore, we had to experiment with different resistive ballasts to prevent the bulb from burning itself out.

Another challenge was writing up the documentation and creating the video has been a very stressful process. As the bulk of the team are high schoolers, this hackathon happened right as finals and AP testing started to kick in. This ate away our time, leaving us only 5 days to write up everything. 

**Edit:** It is with a heavy heart that I write this but it seems that my teammates have ditched me. My teammates promised to help write the documentation, which they wrote the first two paragraphs but disappeared ever since. This is why only one person is listed in the Devpost despite continuously referring to the BrillBox team. I, Kevin Yang, simply assumed that they were taking a break from the screen so I continued to write using “we” and “team”. 
This obviously has its own challenge (I had to do the bulk of the project). 

## Market Evaluation
As said earlier, this product is the only commercially available sterilizer to date. With its simple UI, low price, high user safety, combined with the increased demand for masks, BrillBox is a viable product. 

First and foremost, Brillbox is designed to be manufactured on a large scale. The control circuitry can be easily turned into a PCB and the UV bulbs are in-large supply. This means BrillBox is both cheap to make and always in ready supply. 

Likewise, Brillbox is flexible, able to change form factors depending on the user's needs. If a hospital needs to clean hundreds of masks a day, BrillBox can be easily re-designed to hold a high volume of masks in a dense space, still using the same base controller. If the home user requires only a mask to be cleaned twice a week, a smaller, more compact BrillBox can be made.

Besides flexibility, BrillBox is designed with user safety in mind. As said earlier, the BrillBox team has done their research and has developed a way to safely contain UV light in a box, protecting user’s families, pets, and more. As well, BrillBox can be easily approved by the FDA as it already expounds on best practices seen in lab sterilizers and other commercial UV products such as toothbrush and HVAC cleaners. 

## Improvements
A product can always be improved. With BrillBox, there are a few minor things that need to be improved in later models. 

The first issue is the aluminum foil inside. As the foil layer was done by hand, the aluminum is not as smooth as the team would like. The only consequence of this is a decrease in sanitization efficiency. The un-smooth aluminum foil does not have any effect on the safety of the box.

Likewise, another improvement is using a plastic housing instead of a cardboard box. Although cardboard is cheap and lightweight, it is not as strong as plastic and thus, can be prone to breaking. The reason why Brillbox was constructed using a cardboard box was simply due to a lack of supplies and an inability to get a large, plastic box. 
Another change would be to run the UV bulbs on AC and not DC. The UV bulbs used in BrillBox are some of the most efficient on the market (~40% of the bulb's energy comes out as UV), yet they are currently being run at ½ its rated efficiency. This is simply because the box is driving them using DC whilst they are normally driven off of AC. The reason is simply I did not have access to an AC supply that could power the bulbs. 

The last notable change to Brillbox would be replacing the resistive ballast circuitry with an electric ballast. This would help increase the efficiency of BrillBox as the resistive ballast converts any unneeded current into heat.

## Conclusion
All in all, with Brillbox, users can say goodbye to the days of handwashing masks or going to the store to buy a box of N-95’s. Brillbox is cheap enough, flexible enough, and safe enough to be used by everyone. With the prototype only costing  $11.20 to make, combined with the demand for more PPE and masks, BrillBox will supply the people a product they have been needing for so long. 
	
## Whats Next?
Many say that the COVID-19 pandemic is slowly dying down, but I think the opposite. If we look at the states (in the U.S) that have reopened, many of them have had a huge surge in cases. This is why we need a product such as BrillBox. As long as COVID-19 exists, which will be a while, people will need PPE. BrillBox allows people to reuse their PPE, allowing them to consume less and extend their diminishing supply. 

With that said, I hope to make  BrillBox a fully-fledged consumer product aimed towards at-home users such as families. 

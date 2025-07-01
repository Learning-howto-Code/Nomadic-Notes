## **Total Time Spent:**

## \*I started this project on vacation so for the first few days I didn’t get nearly as much done as you might expect, also I didn’t work on it everyday, so I only included the days I worked on it

# Days 1&2- Gathering intel

	I’ve found that a lot of people 3D print, make pcb’s, and create impressive robotics projects. Some people, especially on youtube create art or even full projects with 3d printing, but very few people create the instructables type projects from a design perspective. Here’s what I mean. If you look online dozens of people have created a weather box for their desk, allowing them to see the weather at a glance. I think this is an awesome project, and will introduce you to electronics, CAD, and integration hell. But they're all just boxes\! For example look at this awesome project by [educ8s on Instructables](https://www.instructables.com/Arduino-ESP32-Color-E-Paper-Weather-Station/). It looks great, and you can really tell that you put a lot of hard work into it. But the actual 3d printed enclosure is quite mundane and is just a box with some light fillets. Just to be clear, I’m not throwing shade on anybody, and especially not educ8s, I think what he did is really cool, but it’s been done before, and not what **I** want to do.  
	So I didn’t. I approached my project from the very beginning as a design project. Yes, there are complicated electronics, enclosures and firmware, but I wanted my project to stand out because it looked good, and for that to be the reason to build it.  
	On days one and two I searched and read nearly every guide on the internet for custom, DIY, portable speakers and a few things stood out to me. Everyone made boomboxes- or at least some version of a big plywood box that housed all the electronics and speakers, meaning that they could never achieve stereo sound nor were they very portable. Also no one made airplay2 speakers. While a proprietary Apple protocol, all of my friends and family, including myself, have iPhones, and if I were to use this speaker regularly it would have to support this super easy way to connect, along with bluetooth. Finally none of them looked good. There were some really nice designs, they weren’t what I was looking for- either they were wood veneer or a retro design. I spent the next few days thinking about how to make my speakers shine.  
 ![image](https://github.com/user-attachments/assets/920131ca-9046-4e44-b5dd-cb02bf99ab2d)
**Time Spent: \~2 hours**

# Days 3 & 4 \- Ideation


From taking 3d sculpture last year in school I learned a lot about planning out a project, and I think it shows how I approached this project that I started with an element of art, sketches; Thumbnail sketches are an easy way to quickly get your ideas on paper, and I love them as their not inhibited by my art skills. From looking at JBl’s website I already knew that I wanted to put a playful spin on the [JBl clip 5](https://www.jbl.com/bluetooth-speakers/CLIP-5.html). I liked the form factor, but knew that it would be near impossible to fit all of my components into such a small form factor, so I decided to take the playful curves and design language of the clip 5 and put a spin on bookshelf speakers. Starting with the shape of a bookshelf speaker, I first thought about putting heavy chamfers on the corners, as seen in the bottom left corner; I decided against this though as chamfers give more of an industrial feel, and suit metal more, which isn’t what I wanted for this project, even though I think it would look really good. I then questioned the form factor, wondering if a tube-like design like the [Charge 5](https://www.jbl.com/bluetooth-speakers/CLIP-5.html) might be better. I also decided against this though, as it has been done before and doesn’t stand out in the way I want it to. You can see that I then settled in on my final design, although it sort of looks like a minion in this drawing. My final design incorporates lots of swooping arches in order to give my speakers the playful look I was going for. In the drawing I played around with color schemes but decided on black and white with orange accents, all PLA.  
![sketches](https://github.com/user-attachments/assets/2a331cad-8948-4cae-8d90-fd2de735338d)
**Time Spent: \~1.5 hours**



# Days 5 & 6 \- Components Sourcing
<img width="322" alt="Screen Shot 2025-07-01 at 1 46 49 PM" src="https://github.com/user-attachments/assets/c51f7977-4b66-4e02-ae0d-e73fac3d0e39" />

	Today I started my [BOM](https://docs.google.com/spreadsheets/d/1EUaRx9kYJ8l8ao9sxJfBVqmWhHC3KokLF9yOrveQJRE/edit?gid=0#gid=0) and sourcing components. After watching videos and reading tutorials I started to get a sense of what components people were using. I finally landed on the Dayton Audio ND65-8 2-1/2" driver from [this video by DIY Perks](https://www.youtube.com/watch?v=a43LXqRwQC8&list=PLOJU8YJjFwGOeh6BgCWVhZf5HSkfVPVP3&index=4&pp=iAQB) as it is a full range driver, eliminating the need for a crossover, while still being quite capable(80-20,000 hertz range). As aforementioned, one of my design requirements was that it had airplay 2, leading me to use a Raspberry Pi 2 W(Rpi) instead of a microcontroller or bluetooth module. The DAC is an important component, since even though the Rpi has built in DAC it’s designed for reading data from the GPIO pins, and isn’t audio grade. I’ve never built a battery pack before, and am deciding to start the CAD first, before sourcing my BMS and charging module.  
**Time Spent\~ 3 hours**

# Days 7 & 8 \- Hoping into CAD
![DIY Speakers pre-render](https://github.com/user-attachments/assets/f61d7dc4-cb78-45c6-bfb7-af9828251d3c)

I use Fusion 360, as I find it’s the perfect tool for these types of projects, plus they hook up students with a free license and cloud computer. After calculating the column for the driver box, I built up the enclosure around it. I designed the whole thing to be assembled with M3 screws, and to print without supports. Before finishing the model I decided to source the last components for my battery pack.

*Render of my mostly complete model*  
**Time Spent \~2 hours**

# Day 9- The battery pack

Today I worked on the battery pack for my speakers. I knew that I wanted to use 18650 cells as I had worked with them before and I found out from the slack that [18650batterystore.com](http://18650batterystore.com) is one of the cheapest places to buy legit cells. After doing some basic math I concluded that my speaker would draw a little less that 5 watts at peak power( 2 watts for the Rpi, 2 watts for the driver, plus some loss along the way). I decided on 4 cells in parallel for an output of 3.7 volts nominal at 10 amps, or around 37 watts. This should give the speakers approximately 7 hours of run time- plenty for an all day battery. After looking at battery packs designed by other people I saw [this super simple one by Great Scott.](https://www.instructables.com/Building-a-USB-Type-C-PD-Powerbank-the-Super-Simpl/) I decided to use the charging IC from it since it would safely charge the 18650 cells, stepped the 3.7 volts up to 5 and charged via Usb-C.  
**Time Spent\~1 hour**

# Day 10- Finishing up CAD
![DIY_Speakers final renderpng](https://github.com/user-attachments/assets/3e90686b-519f-459e-8887-bfa036cb4908)

Today I finished up my CAD design. I added print in place feet to the base of my design and made some other small tweaks. Since I had finalized my battery system I also added things like my rotary encoder and kill switch into the design. Thinking about putting the finishing touches on my design and the acoustic properties of my driver box I studied how high end speakers, like the 2,000$ [Sonus Faber Sonneto’s](https://www.sonusfaber.com/en/products/sonetto-i) use asymmetrical design to dampen resonant frequency and incorporated asymmetrical draft angles into my design to help with frequencies bouncing back and forth between parallel faces. After rendering out my design from a few different angles I was happy with it, and getting ready to submit my project



#### What Will I Learn?
By finishing this tutorial:

♦  The reader will able to create Running lights without the used of arduino

♦  The reader will understand the functions of the circuit and components being used

♦  The reader will be more flexible in using different softwares in components simulations and testings

♦  The reader can be creative in applying this project in the future 


## Introduction
In this tutorial post, we are going to make RUNNING LIGHTS that can be used in different ways like store attractions or simply to beautify anything depends on your creativity and desired application. I made this tutorial post to share another ways of making electronic project not as usual using an arduino. The main components here are 7493 IC and 74154 IC. 7493 IC which is also known as binary counter, will provide a series of changes as pulses was received from the timer circuit while 74154 Demultiplexer will give corresponding output based on the given proper controlled input signal.

You can read more about Running Lights [Here](https://books.google.com.ph/books?id=pmlMOGBrFnAC&pg=PA12&lpg=PA12&dq=running+lights+electronics+using+74154&source=bl&ots=4TXRc8XE01&sig=b6KKUsTS8XrCQkEu715zCamlGdg&hl=en&sa=X&ved=0ahUKEwjHrMnmjs_ZAhUNtJQKHf9zDFQQ6AEISjAH#v=onepage&q=running%20lights%20electronics%20using%2074154&f=false)

![001.PNG](https://steemitimages.com/DQmWYmAruJ2x2bQwXUE9poJ3JKMZRw5HCKNojhzqYdhQUHJ/001.PNG)


#### Requirements
__Materials needed:__

♦ 7493 IC Binary Counter

♦ 74154 Demultiplexer IC

♦ Breadboard (In making Circuit)

♦ Copper Clad Board (Optional)

♦ Jumper wires

♦ Resistors (6pcs of 220 ohms and 1pc of 10k ohms)

♦ Capacitor (10 micro farad)

♦ Potentiometer (100k ohms)

♦ Battery (5v to 9v)



#### Software

♦ Fritzing application
♦ Proteus -  [Direct Download Here](https://drive.google.com/uc?export=download&confirm=wmsG&id=1Hctz4cjR4qLyghdMQQR2H0C92_bpFP0B)

##  Short description for the materials
> [ 7493 IC Binary Counter](https://tams.informatik.uni-hamburg.de/applets/hades/webdemos/30-counters/60-ttl/SN7493.html) ⟶ This ic is responsible in producing a proper controlled signal to the next stage in 74154 Demultiplexer IC.
[74154 Demultiplexer IC](https://www.calstatela.edu/sites/default/files/groups/Department%20of%20Electrical%20and%20Computer%20Engineering/labs/74154.pdf) ⟶It is also called Line DECODER and use to expand an input signal to different output signals.
[Breadboard](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard)  ⟶ It is an electronic tools for experimental purposes where you can make Circuit by experimentally mounting the components, wires and connections temporarily.
[Copper CladBoard](http://www.mpja.com/Copper-Clad-Boards/products/393/) ⟶ It is a board in different sizes where you can sketch your design circuit connections and etch it for permanent layout and permanent circuit connections.
[Jumper Wires](https://en.wikipedia.org/wiki/Jump_wire) ⟶ Wires use for connections to be properly connected and to organize those connections clearly.
[Resistors](http://whatis.techtarget.com/definition/resistor)  ⟶ It is an electronic components responsible in controlling the amount of electrical flow in a certain part of Circuit for the desired amount of voltage.
[Capacitor](https://en.wikipedia.org/wiki/Capacitor)  ⟶  This is an electronic components which stores voltage in electric field.

#### Difficulty

♦ Intermediate

#### Tutorial Contents
Now, I'm going to teach you how to make our RUNNING LIGHTS Circuit using a software called [Proteus](hhttps://en.wikipedia.org/wiki/Proteus_Design_Suite). 

## Part I. Schematic Diagram

❶ Open the Proteus Software
![Screenshot (221).png](https://steemitimages.com/DQmNsDgM583NonqKo7xUHjWoZtMCmyLePLLTHdYLJbTZqi5/Screenshot%20(221).png)

❷ Click on "New Project"

![7.PNG](https://steemitimages.com/DQmPNtDYFwZ2yKPrwcYvm2r5VyEhd9n8oH2xVpcA3gFmncz/7.PNG)

❸ Find and select all the needed Components
>The picture below only shows the main components since the other components are very easy to find by just typing their specific name like resistors, capacitor and LEDs.


![Untitled2.png](https://steemitimages.com/DQmbbqk64qyeUb1EXQs5fkc3Wv6jd5oGetoy4ACjUcqN9CS/Untitled2.png)

#### All Proteus Components needed

![9.PNG](https://steemitimages.com/DQmduSrwTe438GJtgopiPpxrAEr3studwhB9TCRRcT77LHh/9.PNG)

 ❹ Assembling the components
 ###  <center>  First Stage </center>

Actually, The circuit of the project has 3 major stages or parts. The first one is the picture below which is the NE555 area which serves as the timer of the circuit produces pulses depends upon the value combination of resistors.

![11.PNG](https://steemitimages.com/DQmaayQ934fr82x14JKysQLgiBQYAoxzKjUrHRvZf5qrN4i/11.PNG) 
>The purple circle is the Potentiometer which can be adjusted to produce a certain speed of the  frequency. As the resistance increases, the frequency per seconds will becomes slower or smaller while the red arrow represents for the output of this stage.

 ###  <center>  Second Stage </center>
![12.PNG](https://steemitimages.com/DQmSAagQM7UspQn3ZtUpT39jnf8hagQR7aLgmVPSA6AM4Jr/12.PNG)
 In this stage, Referring to 7493 IC, its CKA or clock input receives the pulse signal from the first stage or the timer circuit stage. 

### ***To breifly understand its pin configuration see table below***


##### 7493 (4-bit binary counter)

Pin|Symbol|Description
---------|---------|-------------
1|CKA|clock input, 2nd, 3rd and 4th section (high-to-low edge-triggered)
2	|R0 (1)	|asynchronous master reset
3	|R0 (2)	|asynchronous master reset
4	|NC	|no connection
5	|Vcc	|supply voltage
6	|NC	|no connection
7	|NC|	no connection
8	|QC	|counter output
9	|QB	|counter output
10	|GND	|ground
11	|QD|	counter output
12	|QA|counter output
13	|NC|	no connection
14	|CKB|	clock input, 1st section (high-to-low edge-triggered)

###  <center>  Third Stage </center>

The main component of the third stage is the 74154 Demultiplexer IC. The simple theory behind DEMUX  is just to decode four input signals (signals from 7493) into 16 output signals
This component is very important to produce many outputs from few input frequency signals and for us to make many combinations of led designs.

![16.PNG](https://steemitimages.com/DQmenWFFPUezssv2wgoChNtLwvLeMi9JNvUUNhZCgs2RcrC/16.PNG)

### Notes:
>♦ In wiring the circuit in the real world, make sure not to short the leads of LEDs and resistors because this could damage the Integrated Circuit (IC) permanently.
  

## Part II. Circuit Construction of the Running Lights in BreadBoard

❶ **Open the fritzing Software** - In this part I'm using other type of electronics software for testing components and circuits for Flexibility purposes 🔥. Also, this procedure is for realistic testing of components  connected to each of them in the application of Running lights.
![Screenshot (194).png](https://steemitimages.com/DQmQkok3zPuNEzC9kG2YuomCwLkmck2RReEHkwBuWkbfiaS/Screenshot%20(194).png)

>Beta version can also do the same as the original software

❷ Click on the breadboard
![978978978978.PNG](https://steemitimages.com/DQmWnnmhfNUwe4pgpSyUcohL59J9ohjcgtQd9FG1aL1mhMJ/978978978978.PNG)


❸ Find and ready the components being needed 


![04.PNG](https://steemitimages.com/DQmUgRJr5knskziC6UgqiJiWDF7M6NRGGu1BRVYGqTNj7y1/04.PNG)

❹ Arrange or assemble the components the same connections like the circuit we recently made
 ###  <center>  First Stage </center>
![guide1.jpeg](https://steemitimages.com/DQmcENoLP8fPEo4dGyUJM9f5ndq36FAWyDUosQwcodmPhbg/guide1.jpeg)
>I show this ways to easily analyze and troubleshoot the connections. This will also to guide everyone for the connections to be properly connected

 ###  <center>  Second Stage </center>
![Untitled.jpeg](https://steemitimages.com/DQmTRjXXcHjQ5eDr5ji4nQje82eGdpqGkzcbfjnJk6JRsyV/Untitled.jpeg)
>The same procedure as the first stage, just follow the circuit guide and  just be aware on short circuit to avoid any damage or malfunctions to the circuit.

###  <center>  Third Stage </center>

![LAST.jpeg](https://steemitimages.com/DQmToGBvd2PsV2QBJxqYMjcsXFwArnKLAyTZA2E7RsPjDsF/LAST.jpeg)

<hr>

# <center> The actual Running Lights Project </center>

#### PCB COMPONENTS SIDE
![20180303_000542.jpg](https://steemitimages.com/DQmYkqxVMKXSzj1jxVYQNCasEiUeAW7TPizePSjLRxzourf/20180303_000542.jpg)
>In this picture, you can only see the two (2) ICs because I separated the other one (1) since it takes up much space.

#### PCB SOLDERED SIDE

![20180303_000821.jpg](https://steemitimages.com/DQmbRGaBXiYHfM71Gyz7j5QrCvEub8nVJ4nbxnaDPnGmDgN/20180303_000821.jpg)

#### PARALLEL LEDs

![20180225_132056.jpg](https://steemitimages.com/DQmaD8zPMzw2qKxDBa1LSZEzMWyPXfCMYbkfWLGa9oZf8Z7/20180225_132056.jpg)
>Like I always said, Just be careful and avoid the leads or terminals of any components shorted because it can cause a minor to major damage.

![20180225_132021.jpg](https://steemitimages.com/DQmX6sVaaCpSKVrE34h5UTMC2BkRcJ5WtqjZn4c8R3S1UDo/20180225_132021.jpg)

<hr>

# <center> The Running Lights Actual video </center>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Tc7fnO-gcxM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

>This project is not only limited as what the video shows us. It just wanna help everyone to make your own design depends upon on your creativity and desired uses.

<hr>

# Objective of this project

The main objective of this project is to learn how to design the schematic diagram of running lights circuit at the same time will teach and shows us how to used different softwares  in testing components. This tutorial post will also helps everyone maximize their ability make a project better than this and hopefully apply this project in the future. This project is not limited to this application only , thus it depends on your creativity and desires for the  innovations of our technology/technologies.

I hope that this will be helpful to everyone specially students and fan of Electronics ❤️

# Yours sincerely,

## @thinkvincent


![26756495_1907423502601730_915974359904045118_o.jpg](https://steemitimages.com/DQmVr3noeiVnkrBHr2G1ASwqCfuaPUx83cQDkJSZ4Jukt1B/26756495_1907423502601730_915974359904045118_o.jpg)

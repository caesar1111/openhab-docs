<div class="WordSection1">

<div style="border-style: none none solid; border-color: -moz-use-text-color -moz-use-text-color windowtext; border-width: medium medium 1pt; padding: 0cm 0cm 1pt;">

<span style="position: relative; z-index: 251689984;"><span style="position: absolute; left: 445px; top: -141px; width: 324px; height: 300px;"></span></span><span lang="EN-GB">openHAB2 Raspberry beginner’s walkthrough – (Using Raspberry Pi 3 with openHAB2 and Z-Wave, WiFi LED, Samsung TV and YahooWeather bindings for a home automation project)</span>

</div>

<span lang="EN-GB">Contents</span>

[<span lang="EN-GB">Version index</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">5</span>](#_Toc485150866)

[<span lang="EN-GB">Chapter 1: Before you start</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">6</span>](#_Toc485150867)

[<span lang="EN-GB">Is openHAB2 the right choice for my home automation project?</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">6</span>](#_Toc485150868)

[<span lang="EN-GB">Introduction:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">6</span>](#_Toc485150869)

[<span lang="EN-GB">A few words about the 2 in openHAB2:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">6</span>](#_Toc485150870)

[<span lang="EN-GB">Chapter 2: Preparation</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">7</span>](#_Toc485150871)

[<span lang="EN-GB">Shopping list:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">7</span>](#_Toc485150872)

[<span lang="EN-GB">Minimal setup of the controller:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">7</span>](#_Toc485150873)

[<span lang="EN-GB">Additional hardware for optional setup of the controller with 7” Raspberry display:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">8</span>](#_Toc485150874)

[<span lang="EN-GB">Z-Wave Controller</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">9</span>](#_Toc485150875)

[<span lang="EN-GB">Z-Wave sensors, switches and actuators</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">10</span>](#_Toc485150876)

[<span lang="EN-GB">LAN devices (cable or WiFi)</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">11</span>](#_Toc485150877)

[<span lang="EN-GB">Software list:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">13</span>](#_Toc485150878)

[<span lang="EN-GB">Windows Download list:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">13</span>](#_Toc485150879)

[<span lang="EN-GB">Raspberry downloads:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">13</span>](#_Toc485150880)

[<span lang="EN-GB">Chapter 3: Raspberry hardware and Raspbian OS installation</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">14</span>](#_Toc485150881)

[<span lang="EN-GB">General information about Raspberry interfaces and GPIO pins:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">14</span>](#_Toc485150882)

[<span lang="EN-GB">Raspberry input Overview:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">14</span>](#_Toc485150883)

[<span lang="EN-GB">Raspberry GPIO pin Overview:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">14</span>](#_Toc485150884)

[<span lang="EN-GB">Preparing MicroSD card - writing Raspbian image to MicroSD card (PC required):</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">15</span>](#_Toc485150885)

[<span lang="EN-GB">Connecting the hardware to the Raspberry</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">16</span>](#_Toc485150886)

[<span lang="EN-GB">Basic hardware setup:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">16</span>](#_Toc485150887)

[<span lang="EN-GB">Optional: Installation of 7” Raspberry display and display case:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">17</span>](#_Toc485150888)

[<span lang="EN-GB">Display installation pictures:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">17</span>](#_Toc485150889)

[<span lang="EN-GB">Chapter 4: Raspbian basic configuration</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">21</span>](#_Toc485150890)

[<span lang="EN-GB">Starting up Raspberry or the first time – Raspbian PIXEL desktop</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">21</span>](#_Toc485150891)

[<span lang="EN-GB">Working with the Terminal:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">22</span>](#_Toc485150892)

[<span lang="EN-GB">Basic terminal commands and functions:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">22</span>](#_Toc485150893)

[<span lang="EN-GB">Initial configuration of Raspbian</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">23</span>](#_Toc485150894)

[<span lang="EN-GB">Localisation:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">23</span>](#_Toc485150895)

[<span lang="EN-GB">Optional: Change display orientation</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">24</span>](#_Toc485150896)

[<span lang="EN-GB">Changing Password:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">25</span>](#_Toc485150897)

[<span lang="EN-GB">Enabling interfaces:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">26</span>](#_Toc485150898)

[<span lang="EN-GB">Connect Raspberry to network:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">27</span>](#_Toc485150899)

[<span lang="EN-GB">Check the IP address of the Raspberry:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">27</span>](#_Toc485150900)

[<span lang="EN-GB">Update / Upgrade Raspbian:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">27</span>](#_Toc485150901)

[<span lang="EN-GB">Optional Raspberry settings and configuration:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">28</span>](#_Toc485150902)

[<span lang="EN-GB">Check partition size on MicroSD card:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">28</span>](#_Toc485150903)

[<span lang="EN-GB">Create a Desktop icon and link it to a application</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">28</span>](#_Toc485150904)

[<span lang="EN-GB">Enabling root user:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">29</span>](#_Toc485150905)

[<span lang="EN-GB">Enabling remote SSH access for root user:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">29</span>](#_Toc485150906)

[<span lang="EN-GB">Optional: Raspbian PIXEL screensaver (xscreensaver)</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">30</span>](#_Toc485150907)

[<span lang="EN-GB">Installation of xscreensaver:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">30</span>](#_Toc485150908)

[<span lang="EN-GB">Configuration of xscreensaver:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">30</span>](#_Toc485150909)

[<span lang="EN-GB">Optional: Start Chromium Web server on Raspbian boot</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">31</span>](#_Toc485150910)

[<span lang="EN-GB">Configure the autostart file:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">31</span>](#_Toc485150911)

[<span lang="EN-GB">Select the start URL for Chromium web browser:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">31</span>](#_Toc485150912)

[<span lang="EN-GB">Chapter 5: Setting up Raspbian for access via PC</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">33</span>](#_Toc485150913)

[<span lang="EN-GB">Connect to the Raspberry terminal your windows system using, KiTTY or PuTTY:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">33</span>](#_Toc485150914)

[<span lang="EN-GB">Optional: Connect to the Raspberry file system from your windows system using WinSCP:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">35</span>](#_Toc485150915)

[<span lang="EN-GB">Setup Samba server</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">36</span>](#_Toc485150916)

[<span lang="EN-GB">Common samba server commands:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">36</span>](#_Toc485150917)

[<span lang="EN-GB">Optional: Generic samba user setup</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">37</span>](#_Toc485150918)

[<span lang="EN-GB">Optional: Mapping Raspbian samba directories to Windows (IOS and Linux mapping process can be found online):</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">38</span>](#_Toc485150919)

[<span lang="EN-GB">Chapter 6: Installation of openHAB2 on Raspberry</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">39</span>](#_Toc485150920)

[<span lang="EN-GB">Common openHAB2 service commands:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">40</span>](#_Toc485150921)

[<span lang="EN-GB">openHAB2 configuration for the samba server:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">40</span>](#_Toc485150922)

[<span lang="EN-GB">openHAB2 Privileges for Common Peripherals</span><span lang="ZH-CN" style='font-family: "Times New Roman","serif";'>?</span><span style="color: windowtext; display: none; text-decoration: none;">...</span> <span style="color: windowtext; display: none; text-decoration: none;">41</span>](#_Toc485150923)

[<span lang="EN-GB">Adding openhab user to groupds dialout an tty</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">41</span>](#_Toc485150924)

[<span lang="EN-GB">Granting java environment access to serial ports</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">41</span>](#_Toc485150925)

[<span lang="EN-GB">Chapter 7: Installation of Eclipse Smart Home Designer</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">42</span>](#_Toc485150926)

[<span lang="EN-GB">Installation guide for windows (Eclipse Smart Home Designer and Java Runtime Environment):</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">42</span>](#_Toc485150927)

[<span lang="EN-GB">Launching first time:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">44</span>](#_Toc485150928)

[<span lang="EN-GB">Chapter 8: Initializing openHAB2 (finally: first startup)</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">45</span>](#_Toc485150929)

[<span lang="EN-GB">Chapter 10: General information about configuring openHAB2</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">46</span>](#_Toc485150930)

[<span lang="EN-GB">openHAB (no 2) vs. openHAB2</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">46</span>](#_Toc485150931)

[<span lang="EN-GB">Chapter 10: Configuring openHAB2 using PAPER UI</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">47</span>](#_Toc485150932)

[<span lang="EN-GB">Installing Add-ons</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">47</span>](#_Toc485150933)

[<span lang="EN-GB">General process of adding new things to the configuration</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">49</span>](#_Toc485150934)

[<span lang="EN-GB">Adding local things connected via network (IP)</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">50</span>](#_Toc485150935)

[<span lang="EN-GB">Adding Things using YamahaReceiver Binding:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">50</span>](#_Toc485150936)

[<span lang="EN-GB">Adding Things using Samsung TV Binding:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">51</span>](#_Toc485150937)

[<span lang="EN-GB">Adding Things using WiFi LED Binding:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">52</span>](#_Toc485150938)

[<span lang="EN-GB">Adding online things connected via network (IP)</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">53</span>](#_Toc485150939)

[<span lang="EN-GB">Adding Things using YahooWeather Binding:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">53</span>](#_Toc485150940)

[<span lang="EN-GB">Adding things connected via Z-Wave controller</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">54</span>](#_Toc485150941)

[<span lang="EN-GB">Adding Z-Wave controller</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">54</span>](#_Toc485150942)

[<span lang="EN-GB">Adding Z-Wave things using HABmin UI</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">55</span>](#_Toc485150943)

[<span lang="EN-GB">For details documentation on the Z-Wave Binding usage in HABmin consult:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">56</span>](#_Toc485150944)

[<span lang="EN-GB">Creating items form things</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">57</span>](#_Toc485150945)

[<span lang="EN-GB">The concept of</span> <span lang="EN-US">Things, Channels, Items and Links</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">57</span>](#_Toc485150946)

[<span lang="EN-US">Creating the required items for my project</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">58</span>](#_Toc485150947)

[<span lang="EN-US">Now go on creating the items according to the list below</span><span style="color: windowtext; display: none; text-decoration: none;">..</span> <span style="color: windowtext; display: none; text-decoration: none;">59</span>](#_Toc485150948)

[<span lang="EN-US">Chapter 11: Creating a dashboard for your home automation project</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">60</span>](#_Toc485150949)

[<span lang="EN-US">BASIC UI dashboard</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">60</span>](#_Toc485150950)

[<span lang="EN-US">PAPER UI dashboard</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">61</span>](#_Toc485150951)

[<span lang="EN-US">HABPANEL UI dashboard</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">63</span>](#_Toc485150952)

[<span lang="EN-US">HABMIN dashboard</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">63</span>](#_Toc485150953)

[<span lang="EN-US">Chapter 12: Creating rules</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">64</span>](#_Toc485150954)

[<span lang="EN-GB">Creating the myfirstrule.rules file</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">64</span>](#_Toc485150955)

[<span lang="EN-US">Creating a basic rules</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">66</span>](#_Toc485150956)

[<span lang="EN-US">Basic rule example:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">67</span>](#_Toc485150957)

[<span lang="EN-US">Basic tips for debugging rules</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">70</span>](#_Toc485150958)

[<span lang="EN-US">Creating an item the see the value of a variable of a rule online</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">70</span>](#_Toc485150959)

[<span lang="EN-US">Creating a virtual switch on HABPANEL to use it in a rule</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">72</span>](#_Toc485150960)

[<span lang="EN-US">Further Rule examples based on this home automation project:</span> <span style="color: windowtext; display: none; text-decoration: none;"></span> <span style="color: windowtext; display: none; text-decoration: none;">74</span>](#_Toc485150961)

[<span lang="EN-US">Switching ON/OFF switches based on luminance reading of the multisensory</span><span style="color: windowtext; display: none; text-decoration: none;">.</span> <span style="color: windowtext; display: none; text-decoration: none;">74</span>](#_Toc485150962)

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 14pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

# <a name="_Toc485150866"><span lang="EN-GB">Version index</span></a>

<span lang="EN-GB"> </span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="102" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 76.3pt;">

<span lang="EN-GB">1<sup>st</sup> Draft</span>

</td>

<td width="550" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 412.6pt;">

<span lang="EN-GB">This is the initial version of the document with any feedback of the community.</span>

<span lang="EN-GB">This version was written with the focus on initial hardware and software setup which should already have a good consistency.</span>

<span lang="EN-GB">The openHAB2 configuration and real home automation part still needs some work done!</span>

<span lang="EN-GB">Anyway this part will be the part where you have to apply individual changes and go to the forum for further help since no home automation project is similar to another.</span>

<span lang="EN-GB">You will find not all the bindings utilized and not all the things added to the openHAB2 configuration of the used testbed system since I am building the testbed system again from scratch. So in some places you find pictures missing or description not being completed.</span>

<span lang="EN-GB">I am also using a parallel system (my current live home automation system) to check different hardware configuration, especially when it comes to the displays or to Z-Wave controllers.</span>

_<span lang="EN-GB"> </span>_

_<span lang="EN-GB">Testbed system:</span>_

<span lang="EN-GB">Raspberry Pi 3</span>

<span lang="EN-GB">MicroSD Sandisk Ultra 32GB</span>

<span lang="EN-GB">Power supply goobay 3,1A</span>

<span lang="EN-GB">USB Mouse basic logitech</span>

<span lang="EN-GB">USB Keyboard basic Microsoft qwertz German layout</span>

<span lang="EN-GB">Display HDMI connection to 24” computer display</span>

<span lang="EN-GB">Case no name incl. ventilation</span>

<span lang="EN-GB">Z-Wave controller UZB Z-Wave PLUS USB stick by Z-Wave.Me</span>

<span lang="EN-GB"> </span>

_<span lang="EN-GB">Live home automation system:</span>_

_<span lang="EN-GB">Testbed system:</span>_

<span lang="EN-GB">Raspberry Pi 3</span>

<span lang="EN-GB">MicroSD no name 16GB</span>

<span lang="EN-GB">Power supply no name 3,1A incl. cable swith</span>

<span lang="EN-GB">Bluetooth Keyboard Rapoo Bluetooth Keyboard qwertz German layout</span>

<span lang="EN-GB">Display 7” Raspberry display</span>

<span lang="EN-GB">Case premium case for Raspberry Pi 7" Touch-Display (the closed version)</span>

<span lang="EN-GB">Z-Wave controller Aeotec by Aeon Labs Z-Stick Gen5</span>

<span lang="EN-GB"> </span>

_<span lang="EN-GB">Live Z-Wave devices:</span>_

<span lang="EN-GB">Z-Wave Fibaro Double Switch 2</span>

<span lang="EN-GB">Z-Wave Aeotec by Aeon Labs ZW100 Multisensor</span>

<span lang="EN-GB">Z-Wave Aeon Labs ZW088 Z-Wave Key Fob, Gen5</span>

<span lang="EN-GB">Z-Wave NodOn Smart Plug</span>

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="102" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 76.3pt;">

<span lang="EN-GB">2<sup>nd</sup> Drafty</span>

</td>

<td width="550" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 412.6pt;">

<span lang="EN-GB">Bugfixing (mostly typos)</span>

<span lang="EN-GB">Minor rearranging to content</span>

<span lang="EN-GB">Major changes in</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Chapter 11: Creating a dashboard for your home automation project</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Chapter 12: Creating rules</span>

<span lang="EN-GB">Further input in</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Section “Shopping list”</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Section “Adding local things connected via network (IP)”</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Chapter 12: Creating rules</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 14pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

# <a name="_Toc485150867"><span lang="EN-GB">Chapter 1: Before you start</span></a>

## <a name="_Toc485150868"><span lang="EN-GB">Is openHAB2 the right choice for my home automation project?</span></a>

<span lang="EN-GB">Be aware that openHAB2 is an OPEN home automation solution which is strongly living from a very supportive community. If you want to have a plug and play solution with supplier guaranteed service level and a high likeliness that all the features are working and all the hardware is compatible, you might be better off in getting a ready to use home automation kit including the designated controller (like e.g. devolo or homematic IP). Consider this especially if you are planning to do safety related automation or emergency detection like fire alarm.</span>

<span lang="EN-GB">If you, on the other hand, are willing to spend a few hrs/days in learning how to do a little installation and coding yourself and have no problems with the service level of a Raspberry Pi 3 (it is not as failsafe as other controllers) you might find a perfect environment with openHAB2 for your low cost, very flexible and continuously improving home automation environment.</span>

## <a name="_Toc485150869"><span lang="EN-GB">Introduction:</span></a>

<span lang="EN-GB">This tutorial is targeting beginners like me to get a step by step guideline to get all the things installed. Since I am no coding expert and have no experience in Raspberry and Raspbian I am trying to go through the things step by step, so you should be able to get everything done, even without exactly having to go into all the details. That is one of the reasons I am also using the graphical GUI PIXEL for Raspbian since I thing it makes it easier for the beginners to get started (and you might want to use PIXEL anyway when you are using the Raspberry 7” display as interface for your home automation controller)</span>

<span lang="EN-GB">This tutorial is also based on **having a Windows PC** to support the setup process. You might be able to completely do it without the support of an extra PC, if you can get a MicroSD card with a pre-installed Raspbian OS and use the display options (the Raspberry 7” display or HDMI Display) for the Raspberry.</span>

**<span lang="EN-GB" style="color: red;">DISCLAIMER:</span>**

**_<span lang="EN-GB" style="color: red;">This tutorial might contain some typos, errors or ways of setting up, which can be done in a better way. I am just reflecting my process of starting from scratch and slowly working my way through hundreds of online tutorials, manuals, forum threads etc. and on the way, highlighting the issues I had in getting things working. There will be no guarantee that the given instructions are working for your project as well.</span>_**

<span lang="EN-GB">Anyway I hope this tutorial will help some beginners to enjoy home automation with openHAB2.</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150870"><span lang="EN-GB">A few words about the 2 in openHAB2:</span></a>

<span lang="EN-GB">The 2 in openHAB2 is important! The tutorial is based on the openHAB2 and will not go into all the details of the old version.</span>

<span lang="EN-GB">You just have to be aware, that a lot of online documentation is still for the openHAB version and will **not** be applicable for openHAB2!</span>

<span lang="EN-GB">So the best thing is always to go to the official webpage of openHAB2 and start from there, and only if you really can’t find the information or the link there, go to google and search for other solutions. I was always using the search setting (last year) so it was more likely to the results considering openHAB2 and not openHAB.  
</span>

# <a name="_Toc485150871"><span lang="EN-GB">Chapter 2: Preparation</span></a>

## <a name="_Toc485150872"><span lang="EN-GB">Shopping list:</span></a>

<span lang="EN-GB">As mentioned before, I am basing this tutorial on the graphical GUI of Raspbian named PIXEL so the shopping list is also containing parts for this optional setup:</span>

### <a name="_Toc485150873"><span lang="EN-GB">Minimal setup of the controller:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Raspberry Pi 3</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image002.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">MicroSD card 16GB (minimal to have some buffer for the future) Make sure you have the right card reader to plug the MicroSD card into your computer!</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image003.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Designated Raspberry power supply (min. 2,5A 5V, I recommend 3A) _Do not use other USB chargers since insufficient power supply (shown in GUI as lightening symbol in the upper right corner) will result in serious issues like e.g. Bluetooth not working_) A cable switch might be a good thing since you might have to hard-reset your Pi in the early days more often and the Pi itself does not have a power switch</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image004.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">USB Mouse</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image005.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">USB Keyboard</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image006.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">HDMI cable (full size to whatever your display needs)</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image007.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Ethernet cable (optional, if you not want to use WiFi to connect the Raspberry to your gateway)</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image008.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Raspberry case (optional, will **not** be needed if you are going for the 7” Raspberry display setup)</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image009.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Display with HDMI input ( optional, will **not** be needed if you are going for the 7” Raspberry display setup)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image010.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150874"><span lang="EN-GB">Additional hardware for optional setup of the controller with 7” Raspberry display:</span></a>

<span lang="EN-GB">(I found it very useful to have one permanent GUI interface mounted on your controller, you can also use this touchscreen interface directly to interact with your home automation):</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Raspberry Pi 7" Touch-Display</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image011.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Premium case for Raspberry Pi 7" Touch-Display (closed version) often sold in bundle with Touch-Display, should be available in black, white and transparent</span>

<span lang="EN-GB">This is a very good case if you want to place the controller on a table or counter since it is protecting the Raspberry from the back.</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image012.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image013.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

_<span lang="EN-GB">Alternative:</span>_ <span lang="EN-GB">Cases for Raspberry Pi 7" Touch-Display. You will find a wide range of other cases. The open versions might give you a better access to the Pi GPIO pins or for changing SD card.</span>

<span lang="EN-GB">Please consider: since you can rotate the image of the GUI on the display you can also choose to switch from landscape to portrait orientation</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image014.jpg) ![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image015.jpg) ![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image016.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Bluetooth keyboard (optional, since the optional on screen touch keyboard for Raspbian PIXEL was not working without errors, I decided to go for a Bluetooth keyboard which makes the typing much easier)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image017.jpg)

</td>

</tr>

</tbody>

</table>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150875"><span lang="EN-GB">Z-Wave Controller</span></a>

<span lang="EN-GB">If you want to use the Z-Wave technology for your home automation project you have to have one Z-Wave controller connected to your Raspberry</span>

**<span lang="EN-GB">NOTE</span>**<span lang="EN-GB">: Be aware that the details serial numbers or item names may vary since you have to always make sure to use the hardware which is allowed in your country!</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Aeotec by Aeon Labs Z-Stick Gen5</span>

<span lang="EN-GB">Pros:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Allows offline inclusion of Z-Wave devices which makes it very easy since you only have to take the stick to the mounted device, not the entire Raspberry</span>

<span lang="EN-GB">Cons:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Including battery powered devices into openHAB2 requires a special process (see tutorial)</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image018.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

_<span lang="EN-GB">Alternative</span>_<span lang="EN-GB">: UZB Z-Wave PLUS USB stick by Z-Wave.Me</span>

<span lang="EN-GB">Pros:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Cheapest controller</span>

<span lang="EN-GB">Cons:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">For inclusion, the controller has to be plugged into the Raspberry, so for mounted devices like wall switches , you have to take the Raspberry in close proximity of the device or do the inclusion before you mount the switch inside the wall</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image019.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

_<span lang="EN-GB">NOT REALLY an Alternative</span>_<span lang="EN-GB">: RaZberry2 Z-Wave Plus Daughter Card for Raspberry Pi Home Automation _(not plug and play compatible with optional setup of the controller with 7” Raspberry display!)_</span>

<span lang="EN-GB">Pros:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">will be mounted directly on the Raspberry so it is not using a USB port</span>

<span lang="EN-GB">Cons:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">will be mounted directly on the Raspberry which is blocking the GPIO pins for e.g. the Display power supply or additional cooling fans, so you have to manually solder the power wires at the back of the razberry</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">is using the i/o port of the Raspberry Pi 3 on board Bluetooth, so a lot of additional configuration is needed to get the razberry and the Bluetooth running in parallel.</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">most expensive controller</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span style="position: absolute; z-index: 251636736; margin-left: 47px; margin-top: 12px; width: 95px; height: 86px;">![](openHAB2_Raspberry_beginner-s_walkthrough_files/image020.png)</span>![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image021.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150876"><span lang="EN-GB">Z-Wave sensors, switches and actuators</span></a>

<span lang="EN-GB"> </span>

**<span lang="EN-GB">NOTE</span>**<span lang="EN-GB">: Be aware that the details serial numbers or item names may vary since you have to always make sure to use the hardware which is allowed in your country!</span>

<span lang="EN-GB">Since I am doing a German based home automation project you may find that some Z-Wave devices are not sold in your required country configuration ( e.g. Z-Wave NodOn Smart Plug not available e.g. in the US)</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Z-Wave Fibaro Double Switch 2, Z-Wave Plus Smart Switch (comes at almost the same costs than the single switch and gives you 2 channels. Only reason to go for single switch is you need the full power range of the single switch since the double switch has slightly lower range)</span>

<span lang="EN-GB">NOTE: This switch is designed to be installed in the electrical power wiring of your home (inside a distributor case). In some countries this may only be allowed to be done by special trained staff (insurance and/or law).</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image022.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Z-Wave Aeotec by Aeon Labs ZW100 Multisensor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image023.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Z-Wave Aeon Labs ZW088 Z-Wave Key Fob, Gen5</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image024.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Z-Wave NodOn Smart Plug (not available e.g. in the US)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Z-Wave NodOn Smart Plug, Schalt- und Messsteckdose, Schuko, 1 Stück, NODEMSP3101](openHAB2_Raspberry_beginner-s_walkthrough_files/image025.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">if you want to by other Z-Wave devices always make your they are listed in the Z-Wave device list of the openHAB2 Z-Wave binding to make sure they are supported correctly in the context of openHAB2:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list</span></span>](http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list)

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150877"><span lang="EN-GB">LAN devices (cable or WiFi)</span></a>

<span lang="EN-GB">A lot of things you are using at home are already connected to your LAN and can be integrated into your openHAB2 home automation project if the right binding is available for that device.</span>

<span lang="EN-GB">You can find an overview on</span> [<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/addons/bindings.html</span></span>](http://docs.openhab.org/addons/bindings.html)

**<span lang="EN-GB">NOTE</span>**<span lang="EN-GB">: Be aware that not all the bindings to include devices are already included in the stable version of openHAB2 and may require a manual installation of a so called snapshot version of the binding (how to install snapshot bindings is explained later in this tutorial since we will need it for the WiFi LED controller)</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">WiFi XCSOURCE Magic UFO-WiFi LED-Controller Type LD382 (other brand names might work as well, but you have to make sure it is Type LD382, LD382A or LD686)</span>

<span lang="EN-GB">REMARK: I was using a WiFi controller on purpose since:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">it is only about half the price of a Z-Wave WiFi controller</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">you can control the device as well via smart phone (like light to music feature of the app)</span>

<span lang="EN-GB">But some things you have to be aware of using WiFi LED instead of Z-Wave LED:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">you have to have a WiFi network to which your Raspberry and your WiFi LED controller is connected</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">you have to manually install a beta / snapshot version of openHAB2 or manually install the WiFi LED Binding on top of the package based installation of openHAB2 (see tutorial)</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image026.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">RGB LED stripe incl. power supply 12V DC bundle</span>

<span lang="EN-GB">While you can buy the stripe and the power supply bundle separately, most of the times the bundle will come at the same price or even cheaper. The included power supply plug should directly fit into the power inlet socket of the WiFi controller.</span>

<span lang="EN-GB">REMARK: It also allows you to attach the stripe without soldering since you can just cut the cable of the RGB bundle controller and use it to connect the LED stripe to the WiFi controller.</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![LE 5m 150 5050 Leds Flexibler LED Streifen, RGB, Farbwechsel, DIY-Beleuchtung led strip Inklusive Netzteil und 44 Tasten IR-Fernbedienung, LED Lichtband, Deko, Weihnachten, Party, Ambientbeleuchtung](openHAB2_Raspberry_beginner-s_walkthrough_files/image027.jpg)![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image028.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: White LED stripe</span>

<span lang="EN-GB">Since the WiFi LED-Controller is allowing you to at additionally control plain colour LED stripe (or in case of controller type</span> <span lang="EN-US">LD686</span> <span lang="EN-US"></span> <span lang="EN-GB">even two) you might want to get an additional strip in e.g. plain white to create ab clear white illumination.</span>

<span lang="EN-GB">NOTE: You might be fine with just the stripe if you already got the power supply with the RGB stripe</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![(3,98 €/m) 5m LED Stripe 12V dimmbar - 24W 1200lm - SMD 300 x 3528 60SMD/m - IP20 selbstklebend - 8mm - warmweiß (3000 K)](openHAB2_Raspberry_beginner-s_walkthrough_files/image029.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional (in my case it was already there and I just included it into my project):</span>

<span lang="EN-GB">Yamaha Receiver RX-V581</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image030.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional (in my case it was already there and I just included it into my project):</span>

<span lang="EN-GB">Samsung TV <span style="color: rgb(91, 155, 213);">Details MISSING</span></span>

**<span lang="EN-GB">NOTE:</span> **<span lang="EN-GB">Even when the binding is not officially supporting your TV you might be lucky</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image031.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 14pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150878"><span lang="EN-GB">Software list:</span></a>

<span lang="EN-GB"> </span>

<span lang="EN-GB">My tutorial is using a MS-Windows windows machine for the PC part (You should be able to get it done with Mac or Linux PCs as well, but you have to go online to look up the differences and do some adaptions on the tutorial e.g. mounting the Raspberry file system to PC)</span>

### <a name="_Toc485150879"><span lang="EN-GB">Windows Download list:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">The latest **Raspbian** (Raspberry OS) image</span>

<span lang="EN-GB">You have to download the “Raspbian Jessie with PIXEL - Image with PIXEL desktop based on Debian Jessie” since this tutorial is using PIXEL</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://www.Raspberrypi.org/downloads/Raspbian/</span></span>](https://www.raspberrypi.org/downloads/raspbian/)

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

**<span lang="EN-GB">Etcher</span>** <span lang="EN-GB">(to write the Raspbian image to the SD-Card)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://etcher.io/</span></span>](https://etcher.io/)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

**<span lang="EN-GB">Eclipse Smart HomeDesigner</span>** <span lang="EN-GB">(optional but strongly recommended for easy editing of OpenHAB2 configuration files; incl. syntax highlighting)</span>

<span lang="EN-GB">You have to choose the right version for your PC</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://www.openhab.org/downloads.html</span></span>](https://www.openhab.org/downloads.html)

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">To use Eclipse Smart HomeDesigner you need **Java Runtime Environment JRE** (if not already installed on your PC)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://java.com/</span></span>](https://java.com/)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

**<span lang="EN-GB">PuTTY</span>**

<span lang="EN-GB">or **KiTTY** portable</span>

<span lang="EN-GB">to access the Raspberry console from your PC</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">http://www.putty.org/</span></span>](http://www.putty.org/)

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://portableapps.com/apps/internet/kitty-portable</span></span>](https://portableapps.com/apps/internet/kitty-portable)

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

**<span lang="EN-GB">WinSCP</span>** <span lang="EN-GB">portable to access Raspberry file System directly from your PC (might become obsolete if you use a SAMBA server on your Raspberry, see tutorial)</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://winscp.net/eng/download.php</span></span>](https://winscp.net/eng/download.php)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150880"><span lang="EN-GB">Raspberry downloads:</span></a>

<span lang="EN-GB">How to download software will be explained in the tutorial, but as a reference you will use</span>

**<span lang="EN-GB">openHAB2</span>** <span lang="EN-GB">Package repository based installation or manual installation (be aware that the file locations on the Raspberry will be different based on which kind of installation you choose)</span>

**<span lang="EN-GB">Samba</span>** <span lang="EN-GB">server(for access of Raspberry files from Windows machine; needed for Eclipse Smart HomeDesigner)</span>

**<span lang="EN-GB">xscreensaver</span>** <span lang="EN-GB">(optional if you are using the display setup, to easy control screen blackening or screen savers)</span>

<span lang="EN-GB" style='font-size: 10pt; line-height: 115%; font-family: "Lucida Bright","serif";'> </span>

<span lang="EN-GB" style='font-size: 10pt; line-height: 115%; font-family: "Lucida Bright","serif";'>  
</span>

<span lang="EN-GB" style='font-size: 10pt; line-height: 115%; font-family: "Lucida Bright","serif";'> </span>

# <a name="_Toc485150881"><span lang="EN-GB">Chapter 3: Raspberry hardware and Raspbian OS installation</span></a>

## <a name="_Toc485150882"><span lang="EN-GB">General information about Raspberry interfaces and GPIO pins:</span></a>

### <a name="_Toc485150883"><span lang="EN-GB">Raspberry input Overview:</span></a>

![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image032.jpg)

### <a name="_Toc485150884"><span lang="EN-GB">Raspberry GPIO pin Overview:</span></a>

![Bildergebnis für raspberry pi 3 gpio](openHAB2_Raspberry_beginner-s_walkthrough_files/image033.png)

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150885"><span lang="EN-GB">Preparing MicroSD card - writing Raspbian image to MicroSD card (PC required):</span></a>

<span lang="EN-GB"> </span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="316" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 236.65pt;">

<span lang="EN-GB">Download latest Raspbian Release (*.zip file) to a Windows folder</span>

</td>

<td width="341" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 256.05pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image034.jpg)

</td>

</tr>

<tr>

<td width="316" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 236.65pt;">

<span lang="EN-GB">Extract *.zip file to receive *.img file</span>

</td>

<td width="341" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 256.05pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image035.jpg)

</td>

</tr>

<tr>

<td width="316" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 236.65pt;">

<span lang="EN-GB">Use Etcher to write image to a MicroSD card</span>

1.  <span lang="EN-GB">select image</span>
2.  <span lang="EN-GB">select drive with MicroSD card plugged in to</span>
3.  <span lang="EN-GB">start flashing</span>

</td>

<td width="341" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 256.05pt;">

<span style="font-size: 10pt; line-height: 115%;">![](openHAB2_Raspberry_beginner-s_walkthrough_files/image036.jpg)</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 14pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150886"><span lang="EN-GB">Connecting the hardware to the Raspberry</span></a>

### <a name="_Toc485150887"><span lang="EN-GB">Basic hardware setup:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Connect keyboard and mouse to the USB ports</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image037.jpg)![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image038.jpg)![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image039.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Insert the MicroSD card (pins facing the circuit board)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image003.jpg)![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image040.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Connect Raspberry with display using HDMI ( optional, will **not** be needed if you are going for the 7” Raspberry display setup)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image041.jpg)![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image042.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image043.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Connect the Raspberry with Ethernet cable to your gateway (optional)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image008.jpg)![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image044.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Connect the power supply to the micro USB power input</span>

**<span lang="EN-GB">Make sure that you have everything plugged in and the Raspberry is clear of any metal items since this step is already powering up your Raspberry.</span>**

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Product Details](openHAB2_Raspberry_beginner-s_walkthrough_files/image045.jpg)![Bildergebnis für raspberry pi 3](openHAB2_Raspberry_beginner-s_walkthrough_files/image046.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 14pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150888"><span lang="EN-GB">Optional: Installation of 7” Raspberry display and display case:</span></a>

<span lang="EN-GB">The full tutorial will be found on:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">https://www.element14.com/community/docs/DOC-78156/l/Raspberry-pi-7-touchscreen-display</span></span>](https://www.element14.com/community/docs/DOC-78156/l/raspberry-pi-7-touchscreen-display)

<span lang="EN-GB">and a clip on YouTube:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">https://www.youtube.com/watch?v=tK-w-wDvRTg</span></span>](https://www.youtube.com/watch?v=tK-w-wDvRTg)

**<span lang="EN-GB">Remark</span>**<span lang="EN-GB">: I had an issue with plugging in the power supply to the micro USB power input on the circuit board of the display (like shown in the video). The Raspberry was still showing me the low power symbol (lightening symbol on the upper right corner) SOLUTION:  I had to plug in the power supply to the micro USB power input on the Raspberry itself. The display is now powered via the jumper cables. The standard display case is also allowing for both micro USB power inputs to be used.</span>

**<span lang="EN-GB">NOTE</span>**<span lang="EN-GB">: If the image on the display is having the wrong orientation, you can rotate the image by changing the configuration of Raspbian (see tutorial section Initial configuration of Raspbian)</span>

### <a name="_Toc485150889"><span lang="EN-GB">Display installation pictures:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 1</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp1.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image047.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 2</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp2.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image048.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 3</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp3.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image049.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 4</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp4.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image050.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 5</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp5.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image051.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 6</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp6.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image052.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 7</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![https://files1.element14.com/community/themes/images/piaccessories/PiDisplay_stp7.jpg](openHAB2_Raspberry_beginner-s_walkthrough_files/image053.jpg)

<span lang="EN-GB">The two other path cables (green and yellow can be ignored)</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Step 8</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Assembly of the standard display. (Make sure you have inserted the MicroSD card since you won’t have access to the slot as soon as you mounted the case!)</span>

<span lang="EN-GB">Just pull the back plate off the case, insert the display including the mounted Raspberry (make sure that the path cables and the display cables are not crushed between case and board), tighten it with the 4 screws and put the back plate into place</span>

<span lang="EN-GB">Here is a good clip on YouTube:</span> [<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://www.youtube.com/watch?v=wpSxibZOmoo</span></span>](https://www.youtube.com/watch?v=wpSxibZOmoo)

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150890"><span lang="EN-GB">Chapter 4: Raspbian basic configuration</span></a>

## <a name="_Toc485150891"><span lang="EN-GB">Starting up Raspberry or the first time – Raspbian PIXEL desktop</span></a>

<span lang="EN-GB">Since this tutorial is focussing on using the PIXEL GUI here are a few basic tips</span>

<span lang="EN-GB">Raspberry start-up screen</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image054.jpg)

<span lang="EN-GB">PIXEL basic desktop (including the programs used in this tutorial) not unlike other PC OS desktops:</span>

<span style="position: absolute; z-index: 251685888; margin-left: 346px; margin-top: 19px; width: 152px; height: 167px;">![network configuration](openHAB2_Raspberry_beginner-s_walkthrough_files/image055.png)</span><span style="position: absolute; z-index: 251677696; margin-left: 281px; margin-top: 14px; width: 197px; height: 108px;">![Bluetooth configuration](openHAB2_Raspberry_beginner-s_walkthrough_files/image056.png)</span><span style="position: absolute; z-index: 251669504; margin-left: 77px; margin-top: 13px; width: 158px; height: 100px;">![Terminal](openHAB2_Raspberry_beginner-s_walkthrough_files/image057.png)</span><span style="position: absolute; z-index: 251644928; margin-left: 12px; margin-top: 14px; width: 254px; height: 292px;">![Applications menu (incl. access to configuration)](openHAB2_Raspberry_beginner-s_walkthrough_files/image058.png)</span><span style="position: absolute; z-index: 251661312; margin-left: 56px; margin-top: 14px; width: 96px; height: 175px;">![File manager](openHAB2_Raspberry_beginner-s_walkthrough_files/image059.png)</span><span style="position: absolute; z-index: 251653120; margin-left: 27px; margin-top: 14px; width: 118px; height: 230px;">![Web browser](openHAB2_Raspberry_beginner-s_walkthrough_files/image060.png)</span>![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image061.jpg)

**<span lang="EN-GB"> </span>**

**<span lang="EN-GB">NOTE:</span> **<span lang="EN-GB">If you are working with the 7” Raspberry display setup you might need to flip/rotate the display orientation. Just check the section” Optional: Change display orientation” later in this chapter</span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150892"><span lang="EN-GB">Working with the Terminal:</span></a>

![newdesk](openHAB2_Raspberry_beginner-s_walkthrough_files/image062.jpg)

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">As soon as you have connected the Raspberry to the network you might find it easier to open the Terminal remotely using PuTTY. This also allows you to directly paste command lines from this tutorial into the Terminal. (Right click in PuTTY terminal is pasting the content of the clipboard into the terminal)</span>

### <a name="_Toc485150893"><span lang="EN-GB">Basic terminal commands and functions:</span></a>

<span lang="EN-GB">The full list can be found on:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">https://www.Raspberrypi.org/documentation/linux/usage/commands.md</span></span>](https://www.raspberrypi.org/documentation/linux/usage/commands.md)

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="206" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 154.25pt;">

help

</td>

<td width="451" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB">Is showing you basic commands</span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

sudo _othercommand_

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB">is allowing you to run other commands as super user aka root user</span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

ls -la

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB">Shows the files in a directory incl. additional information</span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-US">cd</span>

<span lang="EN-US"> </span>

<span lang="EN-US">cd</span>

<span lang="EN-US">cd ..</span>

<span lang="EN-US">cd _directory_</span>

_<span lang="EN-US"> </span>_

_<span lang="EN-US">cd /directory/directory</span>_

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB">Is changing the shell working directory.</span>

<span lang="EN-GB">It can be used with attributes:</span>

<span lang="EN-GB">No attribute => working directory is changed to user root directory.</span>

<span lang="EN-GB">working directory is changed to directory one level above</span>

<span lang="EN-GB">working directory is changed to the named</span> _<span lang="EN-US">directory</span>_ <span lang="EN-GB">inside the current directory</span>

<span lang="EN-GB">working directory is changed to the directory defined by the full path</span> _<span lang="EN-US">/directory/directory</span>_

<span lang="EN-GB">.</span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-US">nano _filename_</span>

<span lang="EN-US">(sudo nano _filename)_</span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB">Is stating a basic editor in the terminal to open or create a simple text or configuration file, mostly you have to add a</span> <span lang="EN-US">sudo</span> <span lang="EN-GB">if you want to be able to write the files with root user rights. Closing the editor is done by ctrl+x and then choosing whether you want to save your changes or not</span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-US"> </span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-GB"> </span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-GB"> </span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-GB"> </span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="206" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 154.25pt;">

<span lang="EN-GB"> </span>

</td>

<td width="451" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 338.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 10pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB" style="font-size: 10pt; line-height: 115%;"> </span>

## <a name="_Toc485150894"><span lang="EN-GB">Initial configuration of Raspbian</span></a>

<span lang="EN-GB">The following steps make sure, that basic Raspbian configuration is done.</span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">There may be many tutorials in how to set-up and configure Raspbian and going into more details about user rights and other Raspbian features. This tutorial is showing the way which worked for my project aiming to run openHAB2 on the Raspberry.</span>

<span lang="EN-GB">Since this tutorial is using the PIXEL GUI I always refer to the PIXEL way of configuring and only go back to the terminal way (text only) if it is required.</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150895"><span lang="EN-GB">Localisation:</span></a>

<span lang="EN-GB">The 1.st thing you want to do is changing the localisation settings to make sure your keyboard layout and WiFi settings are matching.</span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Do not change the password before you have changed the keyboard layout since you might put in a different password than you expect (e.g. US qwerty vs. German qwertz results in “Raspberrz” instead of “Raspberry”)</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Raspberry Pi Configuration</span>

<span lang="EN-GB">Application menu</span>

<span lang="EN-GB">-Preferences</span>

<span lang="EN-GB">--Raspberry Pi configuration</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image063.jpg)

</td>

</tr>

<tr style="height: 3.85pt;">

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt; height: 3.85pt;">

<span lang="EN-GB">Go to tab Localisation</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt; height: 3.85pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image064.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select Locale, Timezone, Keyboard and WiFi Country</span>

<span lang="EN-US">Locale</span><span lang="EN-GB">: choose your language and country</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-US">Timezone</span><span lang="EN-GB">: choose timezone</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-US">Keyboard</span><span lang="EN-GB">: choose keyboard language and specific keyboard layout</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-US">WiFi Country</span><span lang="EN-GB">: choose country specific WiFi settings</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image065.jpg)

<span lang="EN-GB"> </span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image066.jpg)

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image067.jpg)

<span lang="EN-GB"> </span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image068.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Accept the reboot</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

**<span lang="EN-GB"> </span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150896"><span lang="EN-GB">Optional: Change display orientation</span></a>

<span lang="EN-GB">If you are working with the 7” Raspberry display setup you might need to flip/rotate the display orientation for specific cases</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image069.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image070.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open boot config.txt file in nano editor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo nano /boot/config.txt</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Add the line at the bottom of the file:</span>

<span lang="EN-GB">(This will flip the display orientation)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

lcd_rotate=2

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: You can choose from different angles</span>

<span lang="EN-GB">    0 degrees rotation</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">  90 degrees rotation</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">180 degrees rotation</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">270 degrees rotation</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">horizontal flip</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">vertical flip</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US"> </span>

<span lang="EN-US">display_rotate=0</span>

<span lang="EN-GB">or</span>

<span lang="EN-US">display_rotate=1</span>

<span lang="EN-GB">or</span>

<span lang="EN-US">display_rotate=2</span>

<span lang="EN-GB">or</span>

<span lang="EN-US">display_rotate=3</span>

<span lang="EN-GB">or</span>

<span lang="EN-US">display_rotate=0x10000</span>

<span lang="EN-GB">or</span>

<span lang="EN-US">display_rotate=0x20000</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Reboot the Raspberry for the changes to take effect</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo reboot

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150897"><span lang="EN-GB">Changing Password:</span></a>

<span lang="EN-GB">This is important to secure your standard Raspberry user “pi” before you connect the Raspberry to the network.</span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Make sure you have changed the keyboard layout to your requirements before change the password.</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Raspberry Pi Configuration</span>

<span lang="EN-GB">Application menu</span>

<span lang="EN-GB">-Preferences</span>

<span lang="EN-GB">--Raspberry Pi configuration</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image071.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Go to tab System and select Change Password (Remark: you might not have the option Expand Filesystem as shown in the picture)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image072.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter initial (for standard user “pi” it is “Raspberry” and your new password</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

Raspberry

_yourpassword_

_yourpassword_

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-family: "Calibri Light","sans-serif";'> </span>**

### <a name="_Toc485150898"><span lang="EN-GB">Enabling interfaces:</span></a>

<span lang="EN-GB">This is required for the communication to the PC (SSH) and to the Z-Wave stick (Serial)</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Raspberry Pi Configuration</span>

<span lang="EN-GB">Application menu</span>

<span lang="EN-GB">-Preferences</span>

<span lang="EN-GB">--Raspberry Pi configuration</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image073.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Go to tab Interfaces</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image074.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enable SSH (to access the Raspberry via Network)</span>

<span lang="EN-GB">Enable Serial (to enable Serial Port for Z-Wave controllers)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

SSH:    Enable

Serial: Enable

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150899"><span lang="EN-GB">Connect Raspberry to network:</span></a><span lang="EN-GB" style="font-size: 10pt; line-height: 112%;"></span>

<span lang="EN-GB" style="font-size: 10pt; line-height: 115%;">Either by plugging in a Ethernet cable or by connecting to a WiFi network:</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB" style="font-size: 10pt;">Click on the network symbol</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB" style="font-size: 10pt;">3 lines and 2 red crosses if no connection is available</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB" style="font-size: 10pt;">Select WiFi network:</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

_yourwifi_

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB" style="font-size: 10pt;">Enter WiFi password</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

_<span style="font-size: 10pt;">yourwifipassword</span>_

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150900"><span lang="EN-GB">Check the IP address of the Raspberry:</span></a>

<span lang="EN-GB">To do so you have to check the IP address of the Raspberry in the terminal</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="262" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Start terminal by clicking on the icon</span>

</td>

<td width="389" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image075.jpg)

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">use the command</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

ifconfig

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Result: the terminal shows you the ip configuration and the IP addresses for the different connections</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<span lang="EN-GB">Ethernet cable:</span> <span lang="EN-US">eth0 _xxx.xxx.xxx.xxx_</span>

<span lang="EN-GB">or</span>

<span lang="EN-GB">WiFi:</span> <span lang="EN-US">wlan0 _xxx.xxx.xxx.xxx_</span>

</td>

</tr>

</tbody>

</table>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">You might want to set your IP address of the Raspberry to static, if you get problems with the lease time setting of your gateway (IP address is changing whenever you reconnect to the network)</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150901"><span lang="EN-GB">Update / Upgrade Raspbian:</span></a>

<span lang="EN-GB">Raspbian is proving online updates so make sure that you have the latest installed before you go further in the configuration.</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="262" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Start terminal by clicking on the icon</span>

</td>

<td width="389" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image075.jpg)

</td>

</tr>

<tr style="height: 56.6pt;">

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt; height: 56.6pt;">

<span lang="EN-GB">use the command</span>

<span lang="EN-GB">(be aware that the upgrade function will take several minutes to complete if you run it for the first time)</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt; height: 56.6pt;">

<span lang="EN-US">sudo apt-get update</span>

<span lang="EN-US">sudo apt-get upgrade</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'>  
</span>**

## <a name="_Toc485150902"><span lang="EN-GB">Optional Raspberry settings and configuration:</span></a>

<span lang="EN-GB">The following settings and configuration is just for additional information and might not be needed to setup openHAB2\. Some of the settings and configuration might still be useful.</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150903"><span lang="EN-GB">Check partition size on MicroSD card:</span></a>

<span lang="EN-GB">Make sure Raspbian is using the full capacity of the MicroSD card (normally while starting up Raspbian for the first time, it is done automatically and the Raspberry will restart automatically):</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="262" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="389" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image077.jpg)

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">use the command</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

sudo fdisk -l

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Result: the terminal shows you the partition size of the two partitions on the MicroSD card summing up to the total capacity</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<span lang="EN-GB">Example for 16 GB:</span>

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">If the capacity is not completely used (e.g. you were using not a plain Raspbian image) you have to expand the partitions manually in the terminal configuration</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Start terminal configuration with command</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

sudo raspi-config

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Select Option (Be aware that the option numbers might change in newer Raspbian releases)</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

7 Advanced Options

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Select Option</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<span lang="EN-US">A1 Expand Filesystem</span>

<span lang="EN-GB">Prompt will tell you that the file system has been increased</span>

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Now select to exit the configuration</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<Finish>

</td>

</tr>

<tr>

<td width="262" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 196.8pt;">

<span lang="EN-GB">Allow reboot</span>

</td>

<td width="389" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 292.1pt;">

<Yes>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150904"><span lang="EN-GB">Create a Desktop icon and link it to a application</span></a><span lang="EN-GB"></span>

<span lang="EN-GB">To be able to create a Icon you have to first create a *.desktop file</span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">This example is creating the desktop icon for the user “pi”</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image078.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image079.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Go to the directory desktop for your “pi” user</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

cd /home/pi/Desktop

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Create a specific desktop file using nano editor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo nano _yourdesktopfile_.desktop

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter parameters into the file accordingly</span>

<span lang="EN-GB">Name:</span> _<span lang="EN-US">YourShortcutName</span>_

<span lang="EN-GB">Comment:</span> _<span lang="EN-US">Your Shortcut Comment</span>_

<span lang="EN-GB">Icon:</span> _<span lang="EN-US">YourIcon</span>_<span lang="EN-US">.png</span>

<span lang="EN-GB">Application for shortcut:</span> <span lang="EN-US">YourShortcutApp</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">Desktop Entry]</span>

<span lang="EN-US">Name=_YourShortcutName_</span>

<span lang="EN-US">Comment=_Your Shortcut Comment_</span>

<span lang="EN-US">Icon=/usr/share/pixmaps/_YourIcon_.png</span>

<span lang="EN-US">Exec=/usr/bin/_YourShortcutApp_</span>

<span lang="EN-US">Type=Application</span>

Encoding=UTF-8

Terminal=false

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-family: "Calibri Light","sans-serif";'> </span>**

### <a name="_Toc485150905"><span lang="EN-GB">Enabling root user:</span></a>

<span lang="EN-GB">Since by default the “root” disabled it can’t be used. You might want to enable it for certain purposes like e.g. enabling the root user for samba file server to get full access to the directories from a PC (see chapter setup samba server)</span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">There is a reason for the “root” being disabled! Enabling the user is allowing full access to the Raspbian and therefore creating a security risk. Please always consider whether you really want to enable this user!</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image080.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Since the user already exists you just have to set the password</span>

<span lang="EN-GB">NOTE: you can also use the command to change the password later on</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo passwd root

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Just enter twice the new password for the “root” user</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

_rootpassword_

_rootpassword_

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150906"><span lang="EN-GB">Enabling remote SSH access for root user:</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">There is a reason for the “root” not being enabled for SSH! Enabling the user for SSH is allowing full remote access to the Raspbian and therefore creating a significant security risk. Please always consider whether you really want to enable this user for SSH!</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image078.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image081.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open sshd.config file in nano editor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo nano /etc/ssh/sshd_config</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Find the section</span> <span lang="EN-US"># Authentication</span> <span lang="EN-GB">in the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US"># Authentication:</span>

<span lang="EN-US">LoginGraceTime 120</span>

<span lang="EN-US">PermitRootLogin without-password</span>

<span lang="EN-US">StrictModes yes</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">And change the</span> <span lang="EN-US">PermitRootLoing</span> <span lang="EN-GB">line to</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

PermitRootLogin yes

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Reboot the Raspberry for the changes to take effect</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo reboot

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150907"><span lang="EN-GB">Optional: Raspbian PIXEL screensaver (xscreensaver)</span></a>

<span lang="EN-GB">If you are working with the 7” Raspberry display setup you might want to use a screensaver as well.</span>

### <a name="_Toc485150908"><span lang="EN-GB">Installation of xscreensaver:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image080.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Install xscreensaver and some additional screen saver themes</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo apt-get install xscreensaver xscreensaver-data-extra xscreensaver-gl-extra</span>

<y>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150909"><span lang="EN-GB">Configuration of xscreensaver:</span></a>

<span lang="EN-GB">I am showing an example configuration which is first switching on a screensaver and then turning off the display completely.</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Screensaver Preferences</span>

<span lang="EN-GB">Application menu</span>

<span lang="EN-GB">-Preferences</span>

<span lang="EN-GB">--Screensaver</span>

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image082.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Configure Display Modes</span>

<span lang="EN-GB">Mode:</span> <span lang="EN-US"><Only One Screen Saver></span>

<span lang="EN-GB">Screensaver:</span> <span lang="EN-US"><Barcode></span>

<span lang="EN-GB">Blank After:</span> <span lang="EN-US"><5></span> <span lang="EN-GB">minutes</span>

<span lang="EN-GB">Cycle After:</span> <span lang="EN-US"><0></span> <span lang="EN-GB">minutes</span>

<span lang="EN-GB">NOTE: This is just a sample configuration selecting one screensaver after 5 minutes</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image083.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Configure Advanced</span>

<span lang="EN-GB">Display Power Management</span>

<span lang="EN-US"><check></span> <span lang="EN-GB">Power Management Enabled</span>

<span lang="EN-GB">Standby After</span> <span lang="EN-US"><10></span> <span lang="EN-GB">minutes</span>

<span lang="EN-GB">Suspend After</span> <span lang="EN-US"><10></span> <span lang="EN-GB">minutes</span>

<span lang="EN-GB">Off After</span> <span lang="EN-US"><10></span> <span lang="EN-GB">minutes</span>

<span lang="EN-US"><check></span> <span lang="EN-GB">Quick Power-off in Blank Only Mode</span>

<span lang="EN-GB"> (Display Power Management)</span>

<span lang="EN-GB">NOTE: This is just a sample switching off the screen after 10 minutes</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image084.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Close the Screensaver Preferences</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150910"><span lang="EN-GB">Optional: Start Chromium Web server on Raspbian boot</span></a>

<span lang="EN-GB"> </span>

### <a name="_Toc485150911"><span lang="EN-GB">Configure the autostart file:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image080.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open the autostart configuration file with nano editor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo nano /home/pi/.config/lxsession/LXDE-pi/autostart</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Add the lines at the end of the file (ignoring error dialogs)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

@unclutter

@chromium-browser --noerrdialogs

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional parameters:</span>

<span lang="EN-GB">--kiosk (for full screen mode. NOTE: to exit full screen mode you have to press “Alt+F4” on the keyboard of the Raspberry, so you have to have a keyboard installed to exit this mode!)</span>

<span lang="EN-GB">--incognito (for incognito mode of the browser)</span>

<span lang="EN-GB">http://yoururl.com (for selecting the URL directly in the configuration file. NOTE: selecting the URL via Chromium settings might be easier)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">@chromium-browser --noerrdialogs --kiosk --incognito http://_yoururl.com_</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Check if the browser is coming up after reboot</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo reboot

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150912"><span lang="EN-GB">Select the start URL for Chromium web browser:</span></a>

<span lang="EN-GB">NOTE: You can also select the URL in the autostart file, but using the browser functionality is giving you a simpler access (no terminal) and you can check the result without rebooting</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="324" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 243.3pt;">

<span lang="EN-GB">Open Chromium and go to the Settings</span>

<span lang="EN-GB">(3 bullets icon)</span>

</td>

<td width="333" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 249.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image085.jpg)

</td>

</tr>

<tr>

<td width="324" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 243.3pt;">

<span lang="EN-GB">Select in the On start-up chapter the option</span>

<span lang="EN-US"><check></span> <span lang="EN-GB">Open a specific page or set of pages</span>

<span lang="EN-GB">And click on the link</span> <span lang="EN-US"><Set pages></span> <span lang="EN-GB">to enter the requested start URL</span>

</td>

<td width="333" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 249.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image086.jpg)

</td>

</tr>

<tr>

<td width="324" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 243.3pt;">

<span lang="EN-GB">Enter the requested start URL</span> _<span lang="EN-US">http://yoururl.com</span>_

<span lang="EN-US"><OK></span> <span lang="EN-GB">your URL</span>

<span lang="EN-GB">Now Chromium is allowing you to enter an additional URL which you can ignore</span>

<span lang="EN-GB"> </span>

</td>

<td width="333" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 249.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image087.jpg)

</td>

</tr>

<tr>

<td width="324" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 243.3pt;">

<span lang="EN-GB">To check if it is working</span>

<span lang="EN-GB">Close Chromium browser</span>

<span lang="EN-GB">Open Chromium browser</span>

<span lang="EN-GB">Result:</span> _<span lang="EN-US">http://yoururl.com</span> _<span lang="EN-GB">should be loaded on startup (in my example I selected the openHAB2 GUI start page )</span>

<span lang="EN-GB">Optional: If you have completed your openHAB2 configuration and want to use HABPANEL as GUI you can just use the URL http://xxx.xxx.xxx.xxx:8080/HABPANEL/index.html#/</span>

<span lang="EN-GB">or even start specific pages in the HABPANEL GUI (just use the URL shown in the browser when you access the HABPANEL page)</span>

</td>

<td width="333" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 249.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image088.jpg)

<span lang="EN-GB">http://_xxx.xxx.xxx.xxx_:8080/start/index</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150913"><span lang="EN-GB">Chapter 5: Setting up Raspbian for access via PC</span></a>

## <a name="_Toc485150914"><span lang="EN-GB">Connect to the Raspberry terminal your windows system using, KiTTY or PuTTY:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="320" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Open KiTTY or PuTTY on your PC</span>

</td>

<td width="337" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image089.jpg)

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Enter Hostname (pi@ in front of the IP is giving the user you want to use for connecting, in this case the standard user “pi”), Port and Connection type</span>

<span lang="EN-GB">Select Open to launch the terminal</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image090.jpg)

<span lang="EN-US">Hostname: pi@_xxx.xxx.xxx.xxx_</span>

<span lang="EN-US">Port:22</span>

<span lang="EN-US">Connection type: SSH</span>

<Open>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Optional save the session</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image091.jpg)

<span lang="EN-GB">Saved session</span> _yoursessionname_

<Save>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">On first connection an security alert is coming which you have to accept</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image092.jpg)

Yes

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Now a terminal window is opening on our PC asking you to enter the “pi” user password</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image093.jpg)

_yourpassword_

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">The terminal window is now starting up in the user home directory</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image094.jpg)

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">You can now use the PC terminal window the same way you us the terminal on the Raspberry itself</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

## <a name="_Toc485150915"><span lang="EN-GB">Optional: Connect to the Raspberry file system from your windows system using WinSCP:</span></a>

**<span lang="EN-GB">NOTE:</span> **<span lang="EN-GB">The connection can only access the rights of the Raspberry user. So the standard user “pi” will not have the writing rights for multiple directories.</span> <span lang="EN-GB" style="font-size: 10pt; line-height: 115%;">For full access you have to use the user “root” (user needs to be enabled since it is disabled in standard setup, procedure shown later in the tutorial), but enabling this user for SSH access is opening up a significant security risk, so it is recommended to use as Raspberry based Samba server for full access to specific directories (shown later in the tutorial).</span>

<span lang="EN-GB"> </span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open WinSCP on your computer</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image095.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select: New Site</span>

<span lang="EN-GB">Select File protocol: SCP</span>

Enter Host name: _xxx.xxx.xxx.xxx_

<span lang="EN-GB">Enter port: 22</span>

<span lang="EN-GB">Enter User name: pi (standard user with limited access to the file system)</span>

<span lang="EN-GB">Enter Password for “pi”</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image096.jpg)

<span lang="EN-GB">File protocol:</span> <span lang="EN-US">SCP</span>

<span lang="EN-GB">Host name:</span> _<span lang="EN-US">xxx.xxx.xxx.xxx</span>_

<span lang="EN-GB">Port:</span> <span lang="EN-US">22</span>

<span lang="EN-GB">User name:</span> <span lang="EN-US">pi</span>

<span lang="EN-GB">Password</span> _<span lang="EN-US">yourpassword</span>_

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional save the Session</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<Save>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">WinSCP is launched showing the windows directory on the left side and the “pi” user home directory of the Raspberry on the right side of the window</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image097.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Lucida Bright","serif";'>  
</span>**

**<span lang="EN-GB" style='line-height: 115%; font-family: "Lucida Bright","serif";'> </span>**

## <a name="_Toc485150916"><span lang="EN-GB">Setup Samba server</span></a>

<span lang="EN-GB">To have access to the Raspberry file system using the PC file explorer (it is needed to run Eclipse Smart Home Designer your PC) you have to setup a Samba server on the Raspberry first.</span>

<span lang="EN-GB">NOTE: You can also follow the alternative instructions for a openHAB2 centric installation at:</span> [<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/installation/linux.html#network-sharing</span></span>](http://docs.openhab.org/installation/linux.html#network-sharing)

<span lang="EN-GB"> </span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image080.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Make sure Raspberry is updated (optional)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo apt-get update

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Download samba server to Raspbery (confirm with enter)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo apt-get install samba samba-common-bin</span>

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open the samba server configuration file in nano editor</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo nano /etc/samba/smb.conf</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Go to the end of the file and add following lines</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">[RaspberryPiDirectories]</span>

<span lang="EN-US">comment = Your full access to Raspberry Pi directories</span>

path = /

read only = no

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional Change the workgroup name if needed, otherwise uncomment and enable WINS support in the section</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US"># Windows Internet Name Serving Support Section:</span>

<span lang="EN-US"># WINS Support - Tells the NMBD component of Samba to enable its WINS Server</span>

<span lang="EN-US">#   wins support = no</span>

<span lang="EN-US">wins support = yes</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Check the syntax of the samba configuration file.</span>

<span lang="EN-GB">Result: there should be no error message(red) in the prompt</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

testparm

<Enter>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Now you have to restart the services to reload the config file</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl restart smbd.service</span>

<span lang="EN-US">sudo systemctl restart nmbd.service</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Make sure that the services are running again without errors</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl status smbd.service</span>

<span lang="EN-US">sudo systemctl status nmbd.service</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150917"><span lang="EN-GB">Common samba server commands:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl status smbd.service</span>

<span lang="EN-US">sudo systemctl status nmbd.service</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Check if all the services are running</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl restart smbd.service</span>

<span lang="EN-US">sudo systemctl restart nmbd.service</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Restart the samba services</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl stop smbd.service</span>

<span lang="EN-US">sudo systemctl stop nmbd.service</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Manually stop the samba services</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

sudo smbpasswd -d _sambausr_

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">If needed: disable a user for samba</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

sudo smbpasswd -e _sambausr_

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">If you need to enable a user for samba</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150918"><span lang="EN-GB">Optional: Generic samba user setup</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Skip this section if you only want to use samba for openHAB2</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Create a special user</span>_<span lang="EN-US">sambausr</span>__ <span lang="EN-US"></span> _<span lang="EN-GB"> for the samba server so you not have to use the root or pi user to allow access to the directories on the Raspberry</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo adduser sambausr

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">You have to enter your password</span>

_<span lang="EN-US">sambausrpassword</span>_ <span lang="EN-GB">and optional information you can just leave empty and finally save with y</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">Adding user `sambausr' ...</span>

<span lang="EN-US">Adding new group `sambausr' (1001) ...</span>

<span lang="EN-US">Adding new user `sambausr' (1001) with group `sambausr' ...</span>

<span lang="EN-US">Creating home directory `/home/sambausr' ...</span>

<span lang="EN-US">Copying files from `/etc/skel' ...</span>

<span lang="EN-US">Enter new UNIX password:</span>

<span lang="EN-US">Retype new UNIX password:</span>

<span lang="EN-US">passwd: password updated successfully</span>

<span lang="EN-US">Changing the user information for sambausr</span>

<span lang="EN-US">Enter the new value, or press ENTER for the default</span>

<span lang="EN-US">        Full Name []:</span>

<span lang="EN-US">        Room Number []:</span>

<span lang="EN-US">        Work Phone []:</span>

<span lang="EN-US">        Home Phone []:</span>

<span lang="EN-US">        Other []:</span>

<span lang="EN-US">Is the information correct?</span> [Y/n] y

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Map the user for Samba with</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo smbpasswd -a sambausr

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter the password</span> _sambausrpassword_

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">New SMB password:</span>

<span lang="EN-US">Retype new SMB password:</span>

Added user sambausr.

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Instead of allowing the</span> _<span lang="EN-US">sambausr</span>_ <span lang="EN-US"></span> <span lang="EN-GB">to have full access on the Raspbian file system to some specific folders by applying the</span> <span lang="EN-US">chown</span> <span lang="EN-GB">command, you might consider enable the root user and use the root user to connect to the Raspberry from the file system (see chapter Optional Raspberry settings and configuration). But be aware that enabling the “root” user is creating a security risk!</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Map the user for Samba with</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo smbpasswd -a root

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter the password</span> _rootpassword_

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">New SMB password:</span>

<span lang="EN-US">Retype new SMB password:</span>

Added user root.

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150919"><span lang="EN-GB">Optional: Mapping Raspbian samba directories to Windows (IOS and Linux mapping process can be found online):</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Skip this section if you only want to use samba for openHAB2</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="320" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">One time map the Raspberry folder to a windows drive (in this case</span> <span lang="EN-US">Z</span><span lang="EN-GB">) enter in the CMD Prompt (just put</span> <span lang="EN-US">CMD</span> <span lang="EN-GB">in the search of Windows 10 to open the command prompt)</span>

</td>

<td width="337" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">net use Z: \\_xxx.xxx.xxx.xxx_\RaspberryPiDirectories /user:sambausr _sambausrpassword_ /persistent:no</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Persistent map the Raspberry folder to a windows drive (in this case</span> <span lang="EN-US">Z</span><span lang="EN-GB">) enter in the CMD Prompt (just put</span> <span lang="EN-US">CMD</span> <span lang="EN-GB">in the search of Windows 10 to open the command prompt)</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-GB">net use Z: \\_xxx.xxx.xxx.xxx_\RaspberryPiDirectories /user:sambausr _sambausrpassword_ /persistent:yes</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">You can also create a simple *.bat file for easy double clicking.</span>

<span lang="EN-GB">Open the editor by just putting</span> <span lang="EN-US">notepad</span> <span lang="EN-GB">in the search of Windows 10</span>

<span lang="EN-GB">Enter the line</span>

<span lang="EN-GB">Save as</span> _<span lang="EN-US">yourmapping</span>_<span lang="EN-US">.bat</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">net use Z: \\_xxx.xxx.xxx.xxx_\RaspberryPiDirectories /user:sambausr _sambausrpassword_ /persistent:no</span>

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150920"><span lang="EN-GB">Chapter 6: Installation of openHAB2 on Raspberry</span></a>

<span lang="EN-GB">This tutorial is only focussing on the package repository installation of the stable version and only on the add-ons for the listed hardware. All other installations are described on the openhab.org site installation for Linux: (</span>[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/installation/linux.html#package-repository-installation</span></span>](http://docs.openhab.org/installation/linux.html#package-repository-installation)<span lang="EN-GB">) For the Raspbian you have to go for the “Apt Based Systems” part of it.</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="291" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="366" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image098.jpg)

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">First, add the openHAB2 bintray repository key to your package manager and allow Apt to use the HTTPS Protocol</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">wget -qO - 'https://bintray.com/user/downloadSubjectPublicKey?username=openhab' | sudo apt-key add -</span>

<span lang="EN-US">sudo apt-get install apt-transport-https</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">I choose the stable Official (Stable) build</span>

<span lang="EN-GB">The stable builds contain the latest official release with tested features.</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">echo 'deb https://dl.bintray.com/openhab/apt-repo2 stable main' | sudo tee /etc/apt/sources.list.d/openhab2.list</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Next, resynchronize the package index:</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

sudo apt-get update

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Now install openHAB2 with the following command:</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">sudo apt-get install openhab2</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Optional but recommended: When you choose to install an add-on, openHAB2 will download it from the internet on request. If you plan on disconnecting your machine from the internet, then you will want to also install the add-ons package.</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">sudo apt-get install openhab2-addons</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Since we were installing the stable version, we have to manually add the binding WIFILED used for the WiFi LED controller manually to the system.</span>

<span lang="EN-GB">First you have to change to the add-ons directory.</span>

<span lang="EN-GB">Than you have to download the latest version of the binding directly from the online repository</span>

<span lang="EN-GB">NOTE: Later, this binding will not be available in the PAPER UI GUI under the Add-ons/Bindings tab, but will show up in the configuration/bindings tab (note here)</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image099.jpg)

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">cd /usr/share/openhab2/addons</span>

<span lang="EN-US">sudo wget https://openhab.ci.cloudbees.com/job/openHAB2-Bundles/lastSuccessfulBuild/org.openhab.binding%24org.openhab.binding.wifiled/artifact/org.openhab.binding/org.openhab.binding.wifiled/2.1.0-SNAPSHOT/org.openhab.binding.wifiled-2.1.0-SNAPSHOT.jar</span>

<span lang="EN-US"> </span>

<span lang="EN-US"> </span>

<span lang="EN-GB">(but here!)</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image100.jpg)

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">If everything went well, you can start openHAB2 and register it to be automatically executed at system startup.</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">sudo systemctl start openhab2.service</span>

<span lang="EN-US">sudo systemctl status openhab2.service</span>

<span lang="EN-US"> </span>

<span lang="EN-US">sudo systemctl daemon-reload</span>

<span lang="EN-US">sudo systemctl enable openhab2.service</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150921"><span lang="EN-GB">Common openHAB2 service commands:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl status openhab2.service</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Shows the status of openHAB2</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl start openhab2.service</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Start the service of openHAB2</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl stop openhab2.service</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Stops the service of openHAB2</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo systemctl restart openhab2.service</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Restarts the service of openHAB2</span>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">sudo apt-get purge openhab2</span>

<span lang="EN-US">sudo rm /etc/apt/sources.list.d/openhab2.list</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">This commands uninstall openHAB2 from your Raspbian</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

## <a name="_Toc485150922"><span lang="EN-GB">openHAB2 configuration for the samba server:</span></a>

<span lang="EN-GB">This is required to grant the PC based Eclipse Smart Home Designer access to the requested configuration folder on your Raspbian.</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="320" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">The shares are configured to be not open for guests nor to the public. Let’s activate the “openhab” user as a samba user</span>

</td>

<td width="337" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

sudo smbpasswd -a openhab

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Enter the password</span> _openhabpassword_

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">New SMB password:</span>

<span lang="EN-US">Retype new SMB password:</span>

Added user openhab.

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Be aware, that creating and later using a specific user will ensure that permissions are honoured. Make sure, the “openhab” user has ownership and/or write access to the openHAB2 configuration files. This can be accomplished by executing:</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">sudo chown -hR openhab:openhab /etc/openhab2</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Restart the samba service to allow the changes to be utilized</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">sudo systemctl restart smbd.service</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">One time map the Raspberry folder to a windows drive (in this case</span> <span lang="EN-US">Z</span><span lang="EN-GB">) enter in the CMD Prompt (just put</span> <span lang="EN-US">CMD</span> <span lang="EN-GB">in the search of Windows 10 to open the command prompt)</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-US">net use Z: \\_xxx.xxx.xxx.xxx_\RaspberryPiDirectories /user:openhab _openhabpassword_ /persistent:no</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Optional: Persistent map the Raspberry folder to a windows drive (in this case</span> <span lang="EN-US">Z</span><span lang="EN-GB">) enter in the CMD Prompt (just put</span> <span lang="EN-US">CMD</span> <span lang="EN-GB">in the search of Windows 10 to open the command prompt)</span>

<span lang="EN-GB">NOTE: Now every time you boot up your PC it will try to connect to the Raspbian samba server.</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-GB" style="font-family: Consolas; color: rgb(112, 173, 71);">net use Z: \\xxx.xxx.xxx.xxx\RaspberryPiDirectories /user:openhab openhabpassword /persistent:yes</span>

</td>

</tr>

<tr>

<td width="320" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.95pt;">

<span lang="EN-GB">Optional: You can also create a simple *.bat file for easy double clicking.</span>

<span lang="EN-GB">Open the editor by just putting</span> <span lang="EN-US">notepad</span> <span lang="EN-GB">in the search of Windows 10</span>

<span lang="EN-GB">Enter the line</span>

<span lang="EN-GB">Save as</span> _<span lang="EN-US">yourmapping</span>_<span lang="EN-US">.bat</span>

</td>

<td width="337" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 252.75pt;">

<span lang="EN-GB" style="font-family: Consolas; color: rgb(112, 173, 71);">net use Z: \\xxx.xxx.xxx.xxx\RaspberryPiDirectories /user:openhab openhabpassword /persistent:no</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150923"><span lang="EN-GB">openHAB2 Privileges for Common Peripherals?</span></a>

<span lang="EN-GB">An openHAB2 setup will often rely on hardware like a modem, transceiver or adapter to interface with home automation hardware. Examples are a Z-Wave, Enocean or RXFcom USB Stick or a Raspberry Pi add-on board connected to the serial port on its GPIOs. In order to allow openHAB2 to communicate with additional peripherals, it has to be added to corresponding Linux groups. The following example shows how to add Linux user openHAB2 to the often needed groups</span> <span lang="EN-US">dialout</span> <span lang="EN-GB">and</span> <span lang="EN-US">tty</span><span lang="EN-GB">. Additional groups may be needed, depending on your hardware and software setup.</span>

### <a name="_Toc485150924"><span lang="EN-GB">Adding openhab user to groupds dialout an tty</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image076.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image080.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter command</span>

<span lang="EN-GB">(This is adding the</span> <span lang="EN-US">openhab</span> <span lang="EN-GB">user to the group</span> <span lang="EN-US">dialout</span><span lang="EN-GB">)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo adduser openhab dialout

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Enter command</span>

<span lang="EN-GB">(This is adding the</span> <span lang="EN-US">openhab</span> <span lang="EN-GB">user to the group</span> <span lang="EN-US">tty</span><span lang="EN-GB">)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo adduser openhab tty

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: Enter command</span>

<span lang="EN-GB">(f you are looking to enable sound privileges for openHAB2, it will also be necessary to add openHAB2 to the “audio” group.)</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

sudo adduser openhab audio

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

### <a name="_Toc485150925"><span lang="EN-GB">Granting java environment access to serial ports</span></a>

<table width="650" class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="329" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Open Terminal</span>

</td>

<td width="321" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

![Ähnliches Foto](openHAB2_Raspberry_beginner-s_walkthrough_files/image078.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image101.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Change to directory</span>

</td>

<td width="321" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

cd /etc/default/

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Open openhab2 file in nano editor</span>

</td>

<td width="321" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

sudo nano openhab2

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Change the text from (nothing between the “”)</span>

<span lang="EN-GB">To (something between the “”)</span>

<span lang="EN-GB"> </span>

</td>

<td width="321" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

<span lang="EN-GB">EXTRA_JAVA_OPTS=""</span>

<span lang="EN-GB">EXTRA_JAVA_OPTS="-Dgnu.io.rxtx.SerialPorts=/dev/ttyUSB0:/dev/ttyS0:/dev/ttyS2:/dev/ttyACM0:/dev/ttyAMA0"</span>

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Exit and save the file</span>

</td>

<td width="321" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

<ctrl+x>

<y>

<Enter>

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Make sure the changes take effect by rebooting the Raspberry</span>

</td>

<td width="321" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 240.95pt;">

sudo reboot

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150926"><span lang="EN-GB">Chapter 7: Installation of Eclipse Smart Home Designer</span></a>

<span lang="EN-GB">(Optional but strongly recommended for easy editing of openHAB2 configuration files; incl. syntax highlighting)</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">The complete installation guide can be found on :</span> [<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/installation/designer.html#setup</span></span>](http://docs.openhab.org/installation/designer.html#setup)

<span lang="EN-GB"> </span>

## <a name="_Toc485150927"><span lang="EN-GB">Installation guide for windows (Eclipse Smart Home Designer and Java Runtime Environment):</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="291" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Download the Windows 64 bit version</span>

</td>

<td width="366" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-GB">http://eclipse.org/downloads/download.php?file=/smarthome/releases/0.8.0/eclipsesmarthome-incubation-0.8.0-designer-win64.zip</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Optional: Download the 32 bit version since there are reports about the “stable” 64 bit version running not stable</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-GB">http://eclipse.org/downloads/download.php?file=/smarthome/releases/0.8.0/eclipsesmarthome-incubation-0.8.0-designer-win.zip</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Optional, but not recommended for beginner: Download a snapshot version</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-GB">https://github.com/eclipse/smarthome/blob/master/docs/documentation/community/downloads.md#designer-builds</span>

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Unzip the downloaded file to a destination of your choice</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

_yourpcdrive:\yourdestionation\_eclipsesmarthome

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Download the offline Java Runtime Environment.</span>

<span lang="EN-GB">Go to the java homepage download section</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Select “See all Java downloads”</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Or directly go to:</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Download the 64bit version (something like jre-8u131-windows-x64.exe ) or the 32bit depending on your system</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://java.com/en/download/</span></span>](https://java.com/en/download/)

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image102.jpg)

<span lang="EN-GB">(</span>[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://java.com/en/download/manual.jsp</span></span>](https://java.com/en/download/manual.jsp)<span lang="EN-GB">)</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image103.jpg)

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Install the Java Runtime Environment to the Eclipse Smart Home Designer folder</span>

<span lang="EN-GB">Start the Java installer</span>

<span lang="EN-GB">Select on the first screen “Change destination folder”</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Change the folder to \jre inside your Eclipse Smart Home Designer folder</span> _<span lang="EN-US">yourpcdrive:\yourdestionation\eclipseSmart Home</span>_<span lang="EN-GB">since this is the loaction your Eclipse Smart Home Designer is expecting the JRE.</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">NOTE: This is now delivering you a “portable” version of the Eclipse Smart Home Designer which just can be copied/moved to different locations or machines without the need of reinstalling.</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image104.jpg)

<Install>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image105.jpg)

<span lang="EN-US"><Change></span>

_<span lang="EN-US">yourpcdrive:\yourdestionation\</span>_<span lang="EN-US">eclipsesmarthome\jre</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

**<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>**

**<span lang="EN-GB"> </span>**

### <a name="_Toc485150928"><span lang="EN-GB">Launching first time:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="291" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Execute the SmartHome-Designer.exe</span>

</td>

<td width="366" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

<span lang="EN-US">yourpcdrive:\yourdestionation\eclipsesmarthome\SmartHome-Designer.exe</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image106.jpg)

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Link the Eclipse Smart Home Designer to the configuration folder on your Raspberry</span>

<span lang="EN-GB">NOTE: Make sure that you have mapped the samba drive before (see openHAB2 setup for the samba server)</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">If you have chosen a different drive letter in the mapping, just replace the Z:</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image107.jpg)

Z:\etc\openhab2

</td>

</tr>

<tr>

<td width="291" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 218.05pt;">

<span lang="EN-GB">Eclipse Smart Home Designer should now recognize the file structure inside the configuration folder and augment the different folders with different icons</span>

</td>

<td width="366" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 274.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image108.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150929"><span lang="EN-GB">Chapter 8: Initializing openHAB2 (finally: first startup)</span></a>

<span lang="EN-GB">To open the openHAB2 you have to access the web GUI with a browser on your PC or directly from your Raspberry, depending on your setup.</span>

<span lang="EN-GB">The URL will be</span> <span lang="EN-US">http://_xxx.xxx.xxx.xxx_:8080/start/index</span> <span lang="EN-GB">filling in the IP of your Raspberry</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="281" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 210.4pt;">

<span lang="EN-GB">First the GUI will ask you to select the initial setup configuration.</span>

<span lang="EN-GB">This will install a standard set of GUIs in openHAB2</span>

<span lang="EN-GB"> </span>

</td>

<td width="376" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 282.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image109.jpg)

</td>

</tr>

<tr>

<td width="281" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 210.4pt;">

<span lang="EN-GB">After a few minutes of installation the standard openHAB2 start GUI will come up, showing you the icons for the pre-installed GUIs:</span>

<span lang="EN-US"><BASIC UI></span>

<span lang="EN-US"><PAPER UI></span>

<span lang="EN-US"><HABPANEL></span>

</td>

<td width="376" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 282.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image110.png)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Now you are ready for the configuration of your home automation project in openHAB2!</span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150930"><span lang="EN-GB">Chapter 10: General information about configuring openHAB2</span></a>

<span lang="EN-GB">Make sure to double check with the official website of openHAB2 since in the end this is where you will find the correct answers if something in this tutorial is not working:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://www.openhab.org/</span></span>](http://www.openhab.org/)

<span lang="EN-GB"> </span>

<span lang="EN-GB">As a start you should read the beginners tutorial form beginning to end so you understand the basic concept of things, items, rules etc. and how they are mend to work together;</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/introduction.html</span></span>](http://docs.openhab.org/introduction.html)

<span lang="EN-GB"> </span>

# <a name="_Toc485150931"><span lang="EN-GB">openHAB (no 2) vs. openHAB2</span></a>

<span lang="EN-GB">One of the most important things I had to learn is that there is also an openHAB (no 2)! So here are a few things if found out to be considerable if you are using openHAB2:</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Always make sure, that you are looking at the right version of openHAB when it comes down to documentation, since a lot of older online documentation is refereeing to the openHAB (no 2). When a few things might be done the same/similar way in openHAB2, other things have changed and will not work in openHAB2</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">You will also encounter two different ways of storing configuration in openHAB.</span>

<span lang="EN-GB" style='font-family: "Courier New";'>o<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">In openHAB (no 2).configuration was stored in files only</span>

<span lang="EN-GB" style='font-family: "Courier New";'>o<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">In openHAB2 you can still use the files, but also can use database storage for certain typs when you do the configuration with PAPER UI. This now might lead to some confusion since you will not be able to change e.g. items in PAPER UI which were configured using a text file. Also you would not have the correct syntax highlighting in the Eclipse Smart Home Designer is expecting file configuration only an items configured in PAPER UI will show up as errors.</span>

<span lang="EN-GB" style='font-family: "Courier New";'>o<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">But be aware that some configuration in openHAB2 still has to be done via text file like e.g. rules. You might find already some progress in the snapshot release of openHAB2, but I decided to base this tutorial on the stable release with limited functionality in PAPER UI database</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Regularly check the website of openHAB2 for news since a lot of new features are expected to be implemented.</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">Meanwhile be not afraid to go and sign up the openHAB community:</span> <span lang="EN-GB"></span> [<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">h</span></span><span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">ttps://community.openhab.org</span></span>](https://community.openhab.org) <span lang="EN-GB">and ask your questions there. I got replies to my problems within days, sometimes even within hrs. There is also a designated area for beginners.</span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

# <a name="_Toc485150932"><span lang="EN-GB">Chapter 10: Configuring openHAB2 using PAPER UI</span></a>

<span lang="EN-GB">Since the online documentation is mostly referring to PAPER UI GUI I will try to stick to this GUI as long as possible.</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">HABmin GUI will be needed for some  Z-Wave installation</span>

<span lang="EN-GB">-<span style='font-family: "Times New Roman"; font-style: normal; font-variant: normal; font-weight: normal; font-size: 7pt; line-height: normal; font-size-adjust: none; font-stretch: normal;'></span> </span><span lang="EN-GB">HABPANEL GUI will be used to create the final user frontend for this project</span>

<span lang="EN-GB">NOTE: Since you will be regularly starting and switching the GUIs I highly recommend creating quick links in your browser for each GUI</span>

## <a name="_Toc485150933"><span lang="EN-GB">Installing Add-ons</span></a><span lang="EN-GB"></span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="329" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Start PAPER UI</span>

<span lang="EN-GB"> </span>

</td>

<td width="328" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

<span lang="EN-GB">http://xxx.xxx.xxx.xxx:8080/paperui/index.html#/inbox/search</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image111.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Select</span>

<span lang="EN-GB">-Add-ons</span>

<span lang="EN-GB">--Bindings</span>

<span lang="EN-GB">and install the Bindings:</span>

<span lang="EN-GB"><Samsung TV Binding></span>

<span lang="EN-GB"><YahooWeather Binding></span>

<span lang="EN-GB"><YamahaReceiver Binding></span>

<span lang="EN-GB"><Z-Wave Binding></span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image112.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Result:</span>

<span lang="EN-GB">The icons of the bindings should change to blue</span>

<span lang="EN-GB">The install option should change to uninstall</span>

<span lang="EN-GB">(sometimes you have to reload the page if the update is not coming up for a few minutes)</span>

<span lang="EN-GB">NOTE: Since in my project case, the Yamaha Receiver is already connected to the same network than my Raspberry, I do already get a message in the inbox which is telling me, that a new thing was found</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image113.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Select</span>

<span lang="EN-GB">-Add-ons</span>

<span lang="EN-GB">--User Interfaces</span>

<span lang="EN-GB">and install the User Interface HABmin</span>

<span lang="EN-GB">which we will need for some Z-Wave stuff</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image114.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Result:</span>

<span lang="EN-GB">HABmin GUI is installed</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image115.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150934"><span lang="EN-GB">General process of adding new things to the configuration</span></a>

<span lang="EN-GB">NOTE: If you can add new things to openHAB2 depends on whether they are connected to the network (if you use IP), whether they are included in the Z-Wave network of the Z-Wave controller or whether your Raspberry is online if you use online sourced like YahooWeather</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Since in my project case, the Yamaha Receiver is already connected to the same network than my Raspberry, I do already get a message in the inbox which is telling me, that a new thing was found</span>

<span lang="EN-GB">Now just click on the blue icon with the check mark to add this thing</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image116.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">You can now change the name of the thing if you want to</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image117.jpg)

<ADD AS THING>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">If the thing is not found automatically, you have to add it using the blue add icon (+) to manually add a thing.</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image118.jpg)

<(+)>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">This will now show you all the installed Bindings which can be used to add more things.</span>

<span lang="EN-GB">NOTE: You should find all bindings there which we installed in the step Installing Add-ons.</span>

<span lang="EN-GB">Additionally you will find the</span> <span lang="EN-US"><WiFi LED Binding>,</span> <span lang="EN-GB">which we manually installed in “Chapter 6: Installation of openHAB2 on Raspberry” since this is a snapshot Binding which we managed manually</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image119.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150935"><span lang="EN-GB">Adding local things connected via network (IP)</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Make sure that the device is connected to the Raspberry network via IP.</span>

### <a name="_Toc485150936"><span lang="EN-GB">Adding Things using YamahaReceiver Binding:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">The thing should come up automatically in you inbox as soon as you connect it to the network</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image120.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">You can now change the name of the thing if you want to</span>

<span lang="EN-GB">You can also change the name of the thing if you are planning to run with your own naming convention</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image121.jpg)

<ADD AS THING>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: Select in your PAPER UI inbox the add blue add icon (+)</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Search for the thing manually using the YamahaReceiver Binding</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image122.jpg)

<(+)>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image123.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">tab and check whether the now thing is available.</span>

<span lang="EN-GB">The green icon online next to the name is indicating that openHAB2 is connected to the thing and information can be exchanged</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image124.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-family: "Calibri Light","sans-serif";'> </span>**

### <a name="_Toc485150937"><span lang="EN-GB">Adding Things using Samsung TV Binding:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">The thing should come up automatically in you inbox as soon as you connect it to the network</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Picture MISSING](openHAB2_Raspberry_beginner-s_walkthrough_files/image125.png)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">You can now change the name of the thing if you want to</span>

<span lang="EN-GB">and add the thing.</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Picture MISSING](openHAB2_Raspberry_beginner-s_walkthrough_files/image125.png)

<ADD AS THING>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: Select in your PAPER UI inbox the add blue add icon (+)</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Search for the thing manually using the Samsung TV Binding</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image122.jpg)

<(+)>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image126.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">tab and check whether the now thing is available.</span>

<span lang="EN-GB">The green icon online next to the name is indicating that openHAB2 is connected to the thing and information can be exchanged</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![Picture MISSING](openHAB2_Raspberry_beginner-s_walkthrough_files/image125.png)

</td>

</tr>

</tbody>

</table>

### <span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB" style='font-family: "Calibri Light","sans-serif";'> </span>

### <a name="_Toc485150938"><span lang="EN-GB">Adding Things using WiFi LED Binding:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">The thing should come up automatically in you inbox as soon as you connect it to the network</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image127.jpg)

<(+)>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">You can now change the name of the thing if you want to</span>

<span lang="EN-GB">and add the thing.</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image128.jpg)

<ADD AS THING>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Optional: Select in your PAPER UI inbox the add blue add icon (+)</span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">Search for the thing manually using the Samsung TV Binding</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image122.jpg)

<(+)>

<span lang="EN-GB"> </span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image129.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">tab and check whether the now thing is available.</span>

<span lang="EN-GB">The green icon online next to the name is indicating that openHAB2 is connected to the thing and information can be exchanged</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image130.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150939"><span lang="EN-GB">Adding online things connected via network (IP)</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">Make sure the Raspbian does have online access pages.</span>

### <a name="_Toc485150940"><span lang="EN-GB">Adding Things using YahooWeather Binding:</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select in your PAPER UI inbox the add blue add icon (+)</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image131.jpg)

<(+)>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select the Binding</span> <span lang="EN-US"><YahooWeather Binding></span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image132.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select the thing</span> <span lang="EN-US"><Weather Information></span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image133.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Now you have to configure the thing</span>

<span lang="EN-GB">In this case you have to enter the WOEID which is a 32-bit reference identifier of the location you want to see the weather information for.</span>

<span lang="EN-GB">You can look up the WOEID on e.g.</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">http://www.woeidlookup.com/</span></span>](http://www.woeidlookup.com/)

<span lang="EN-GB"> </span>

<span lang="EN-GB">In this case we choose Berlin</span>

<span lang="EN-GB">WOEID:</span> <span lang="EN-US">638242</span>

<span lang="EN-GB">More information on WOEID on:</span>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; color: windowtext; text-decoration: none;">https://en.wikipedia.org/wiki/WOEID</span></span>](https://en.wikipedia.org/wiki/WOEID)

<span lang="EN-GB"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image134.jpg)

638242

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Then just add the thing by clicking on the blue check icon</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image135.jpg)

<(+)>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">tab and check whether the now thing is available.</span>

<span lang="EN-GB">The green icon online next to the name is indicating that openHAB2 is connected to the thing and information can be exchanged</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image124.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-GB" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150941"><span lang="EN-GB">Adding things connected via Z-Wave controller</span></a>

**<span lang="EN-GB">NOTE:</span>** <span lang="EN-GB">first you have to connect the Z-Wave controller as a thing. After this you will use HABmin to further include things into the Z-Wave network. These things should show up automatically in the inbox of PAPER UI.</span>

### <a name="_Toc485150942"><span lang="EN-GB">Adding Z-Wave controller</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select in your PAPER UI inbox the add blue add icon (+)</span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image122.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select the Binding</span> <span lang="EN-US"><Z-Wave Binding></span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image136.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Select the thing</span> <span lang="EN-US"><Z-Wave Serial Controller></span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image137.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Now you have to configure the thing</span>

<span lang="EN-GB">In this case you have to enter the serial Port of the Z-Wave controller</span>

<span lang="EN-GB">The standard port where the UBS-Z-Wave controller should come up it:</span>

/dev/ttyACM0

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image138.jpg)

/dev/ttyACM0

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Then just add the thing by clicking on the blue check icon</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image139.jpg)

<(+)>

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">tab and check whether the now thing is available.</span>

<span lang="EN-GB">The green icon online next to the name is indicating that openHAB2 is connected to the thing and information can be exchanged</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image140.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150943"><span lang="EN-GB">Adding Z-Wave things using HABmin UI</span></a>

<span lang="EN-GB">To include further devices into your Z-Wave network and make the available as openHAB2 things you have to use the HABmin inclusion functionality.</span>

<span lang="EN-GB">Please also consult the online documentation for general information about Z-Wave :</span> [<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">https://github.com/openhab/org.openhab.ui.habmin/wiki/ZWave-Device-Installation</span></span>](https://github.com/openhab/org.openhab.ui.habmin/wiki/ZWave-Device-Installation)

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="329" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Start HABmin</span>

<span lang="EN-GB">Direct URL:</span> <span lang="EN-US">http://xxx.xxx.xxx.xxx:8080/habmin/index.html#/home</span>

<span lang="EN-GB">The select the Things tab</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-GB">HABmin will show you all the things which are available in PAPER UI as well</span>

</td>

<td width="328" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image141.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">To start the inclusion in HABmin you have to select the add thing icon of HABmin (magnifying glass)</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image142.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Then select the Z-Wave binding</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image143.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">This now is triggering the inclusion mode of your Z-Wave controller</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image144.jpg)

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image145.jpg)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Now you have to put your Z-Wave devices in inclusion mode to be detected for online detection</span>

<span lang="EN-GB">(applicable when using UZB Z-Wave PLUS USB stick by Z-Wave.Me as a Z-Wave controller</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

<span lang="EN-GB">Please refer to the Z-Wave devices manual how to put them in inclusion mode</span>

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">Optional: Using the Aeotec by Aeon Labs Z-Stick Gen5 which is allowing for offline inclusion</span>

<span lang="EN-GB">Since this Z-Wave controller stick is allowing for offline inclusion, you have to unplug the stick before you start the inclusion on HABmin and use the inclusion button on the stick to start the inclusion mode inclusion mode of your Z-Wave controller</span>

<span lang="EN-GB">The plug in the stick again do the HABmin inclusion. You do not have to put your Z-Wave devices again in inclusion mode.</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

<span lang="EN-US">Please refer to the</span> <span lang="EN-GB">Aeotec by Aeon Labs Z-Stick Gen5 documentation for further details</span>

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">And when a device is found it will be listed</span>

<span lang="EN-GB">Just select the <Add> button to include this device as a thing for openHAB2</span>

<span lang="EN-GB">NOTE: some devices may come up as **“unknown device”**. You can still add the device and “cure” the information later.</span>

<span lang="EN-GB">The normal reason for this is that the device was not able to finish the communication with HABmin during the inclusion process</span>

<span lang="EN-GB">This might be very likely for battery powered devices since the will go to sleep mode after a certain amount of time. To cure this you just have to manually wake up the device (see device manual) multiple times (up to 10 times) before the communication is completed and the device is recognized as a proper thing in HABmin</span>

<span lang="EN-GB">ATTENTION: Using the **Aeotec by Aeon Labs Z-Stick Gen5** almost every battery powered item will come up as **“unknown device”** since in the timespan you include the battery device to the stick and you do the HABmin inclusion after you plugged the stick back in will be to long an most of the devices will go back to sleep. You might prevent this by manually waking up the device again just seconds before you start the inclusion on HABmin.</span>

<span lang="EN-GB">The other reason is that the device is not supported by the openHAB2 Z-Wave binding. You can check the supported devices at:</span>

<span lang="EN-US">http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

![http://www.cd-jackson.com/images/habmin/HABmin-Things-discovery_inbox.png](openHAB2_Raspberry_beginner-s_walkthrough_files/image146.png)

</td>

</tr>

<tr>

<td width="329" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 246.4pt;">

<span lang="EN-GB">The newly added thing should now be visible in the HABmin GUI things tab</span>

<span lang="EN-GB">Now you can switch to the PAPER UI and find the new things in the inbox or check the new things in the things tab</span>

</td>

<td width="328" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 246.3pt;">

<span lang="EN-GB"> </span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

### <a name="_Toc485150944"><span lang="EN-GB">For details documentation on the Z-Wave Binding usage in HABmin consult:</span></a>

[<span class="Heading9Char"><span lang="EN-GB" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://www.cd-jackson.com/index.php/openhab/habmin/10-habmin-zwave-binding-initialisation</span></span>](http://www.cd-jackson.com/index.php/openhab/habmin/10-habmin-zwave-binding-initialisation)

<span lang="EN-GB"> </span>

<span lang="EN-GB" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-GB"> </span>

## <a name="_Toc485150945"><span lang="EN-GB">Creating items form things</span></a>

### <a name="_Toc485150946"><span lang="EN-GB">The concept of</span> </a><span lang="EN-US">Things, Channels, Items and Links</span>

<span lang="EN-GB">Before we start please read first the concept of</span> <span lang="EN-US">Things, Channels, Items and Links which is directly tanken from the openHAB2 User Manual page</span> [<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/concepts/index.html#things-channels-items-and-links</span></span>](http://docs.openhab.org/concepts/index.html#things-channels-items-and-links)<span lang="EN-US"></span>

<span lang="EN-US">Things are the entities that can be physically added to a system and which can potentially provide many functionalities at once. It is important to note that things do not have to be devices, but they can also represent a web service or any other manageable source of information and functionality. Things provide their functionality through a set of Channels. Channels are “passive” and can be regarded as a declaration of a Thing, what it can offer. It is up to the individual setup, which of the Channels are actively used through Items (see below).</span>

<span lang="EN-US">Items represent (fine-grained) functionality that is used by applications - as user interfaces or automation logic. Items have a state and they can receive commands.</span>

<span lang="EN-US">The glue between Things and Items are Links. Links are associations between exactly one Thing Channel and one Item. If a Channel is linked to an Item, it is “enabled”, which means that the functionality that the Item represents is handled through the given Channel. Channels can be linked to multiple Items and Items can be linked to multiple Channels.</span>

<span lang="EN-US">To illustrate these concepts, take a two-channel actuator that controls two lights:</span>

![http://docs.openhab.org/concepts/images/thing-devices-1.png](openHAB2_Raspberry_beginner-s_walkthrough_files/image147.png)

<span lang="EN-US">The actuator is the Thing. This might be installed in the electrical cabinet, it has a physical address and needs to be setup and configured in order to be used. The user is instead interested in the two lights, which are located at different locations in his home. These lights are the desired functionality, thus the Items and they are linked to the Channels of the actuator. A Link can be regarded like a physical wire in this example.</span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

<span lang="EN-US">The basic process of in PAPER UI is explained on:</span> [<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/tutorials/beginner/configuration.html</span></span>](http://docs.openhab.org/tutorials/beginner/configuration.html)<span lang="EN-US"></span>

### <a name="_Toc485150947"><span lang="EN-US">Creating the required items for my project</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="326" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-GB">Switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Things</span>

<span lang="EN-US">and select the KeyFob_Gen5 thing</span>

<span lang="EN-US"> </span>

</td>

<td width="326" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image148.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">A list of all the available channels of the thing will be shown</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span style="position: absolute; z-index: 251686912; margin-left: 19px; margin-top: 15px; width: 19px; height: 24px;">![](openHAB2_Raspberry_beginner-s_walkthrough_files/image149.jpg)</span>![](openHAB2_Raspberry_beginner-s_walkthrough_files/image150.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">Now click on the blue icon in front of the channel number to link this channel to an item</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span style="position: absolute; z-index: 251688960; margin-left: 19px; margin-top: 15px; width: 19px; height: 20px;">![](openHAB2_Raspberry_beginner-s_walkthrough_files/image151.jpg)</span>![](openHAB2_Raspberry_beginner-s_walkthrough_files/image150.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">A link channel window will come up</span>

<span lang="EN-US">Select the pull down option for the item</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

<span style="position: absolute; z-index: 251687936; margin-left: 19px; margin-top: 95px; width: 18px; height: 19px;">![](openHAB2_Raspberry_beginner-s_walkthrough_files/image152.jpg)</span>![](openHAB2_Raspberry_beginner-s_walkthrough_files/image153.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">The next window coming up will allow you to select already existing items or:</span>

<span lang="EN-US">In our case <+Create new item…></span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

**![](openHAB2_Raspberry_beginner-s_walkthrough_files/image154.jpg)**

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">The next window will allow you to configure the item you want to link to the thing channel</span>

<span lang="EN-GB">You can also change the name of the item if you are planning to run with your own naming convention</span>

<span lang="EN-GB">Then select <LINK> to create your new item</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image155.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">Now the blue icon to the left of the name will change (white dot in the center)</span>

<span lang="EN-US">By clicking on this icon the channel will expand and show you the linked items to this cannel</span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image156.jpg)

</td>

</tr>

<tr>

<td width="326" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 244.45pt;">

<span lang="EN-US">You can now find the new item in</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Items</span>

<span lang="EN-US"> </span>

</td>

<td width="326" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 244.45pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image157.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

### <a name="_Toc485150948"><span lang="EN-US">Now go on creating the items according to the list below</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="196" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 147.15pt;">

<span lang="EN-US">Thing</span>

</td>

<td width="276" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">Channel</span>

</td>

<td width="185" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">Item</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

KeyFob_Gen5

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node9:scene_number</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

KeyFob_Gen5_SceneNumber

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Weather Information

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

yahooweather:weather:c5d26906:temperature

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

Yahoo_Temperature

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Weather Information

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

yahooweather:weather:c5d26906:humidity

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

Yahoo_Humidity

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Yamaha Receiver RX-V581

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">yamahareceiver:yamahaAV:9ab0c000_f668_11de_9976_00a0dedc57ff:power</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

YamahaReceiverRXV581_Power

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Yamaha Receiver RX-V581

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">yamahareceiver:yamahaAV:9ab0c000_f668_11de_9976_00a0dedc57ff:volume</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

YamahaReceiverRXV581_Volume

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Yamaha Receiver RX-V581

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">yamahareceiver:yamahaAV:9ab0c000_f668_11de_9976_00a0dedc57ff:mute</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

YamahaReceiverRXV581_Mute

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

<span lang="EN-US">Z-Wave Node 2: FGS223 Double Switch 2</span>

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node2:meter_watts</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

DoubbleSwitch01_LeistungGesamt

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

<span lang="EN-US">Z-Wave Node 2: FGS223 Double Switch 2</span>

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node2:switch_binary1</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

DoubbleSwitch01_Relais1

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

<span lang="EN-US">Z-Wave Node 3: MSP-3-1-X1 Z-Wave Plus Micro Smart Plug ON/OFF</span>

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node3:switch_binary</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

SchuKo01

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

<span lang="EN-US">Z-Wave Node 3: MSP-3-1-X1 Z-Wave Plus Micro Smart Plug ON/OFF</span>

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node3:meter_watts</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

SchuKo01_Leistung

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Z-Wave Node 6: ZW100 MultiSensor 6

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node6:sensor_relhumidity</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">MultiSens_Luftfeuchte</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Z-Wave Node 6: ZW100 MultiSensor 6

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node6:sensor_temperature</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">MultiSens_Temperatur</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

Z-Wave Node 6: ZW100 MultiSensor 6

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">zwave:device:39e18a8c:node6:sensor_luminance</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">MultiSens_Helligkeit</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

HF-LPB100-ZJ200

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">wifiled:wifiled:F0FE6B314910:power</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">HFLPB100ZJ200_Power</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

HF-LPB100-ZJ200

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">wifiled:wifiled:F0FE6B314910:color</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">HFLPB100ZJ200_Color</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

HF-LPB100-ZJ200

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US">wifiled:wifiled:F0FE6B314910:white</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span lang="EN-US">HFLPB100ZJ200_White</span>

</td>

</tr>

<tr>

<td width="196" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 147.15pt;">

<span style="color: rgb(91, 155, 213);">DUMMYTHING_SamsungTV</span>

</td>

<td width="276" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 206.9pt;">

<span lang="EN-US" style="color: rgb(91, 155, 213);">Data missing</span>

</td>

<td width="185" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 138.65pt;">

<span style="color: rgb(91, 155, 213);">DUMMYITEM_SamsungTV_Power</span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

# <a name="_Toc485150949"><span lang="EN-US">Chapter 11: Creating a dashboard for your home automation project</span></a>

<span lang="EN-US">Every User Interface on openHAB2 is providing its own style of dashboards to control your home automation project, display current item states and attribute values or even include online information like web pages.</span>

<span lang="EN-US">In our configuration of openHAB2 you will have the choice of 4 different user interfaces which can be selected</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="319" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 239.3pt;">

<span lang="EN-GB">Start openHAB2 start screen</span>

<span lang="EN-GB">Direct URL:</span> <span lang="EN-US">http://xxx.xxx.xxx.xxx:8080/ start/index</span>

<span lang="EN-US">Here you will now find the GUIs:</span>

<span lang="EN-US"><BASIC UI></span>

<span lang="EN-US">(requires setup using textual *.sitemap files)</span>

<span lang="EN-US"><PAPER UI></span>

<span lang="EN-US">(which were already using to configure openHAB2)</span>

<span lang="EN-US"><HABPANEL></span>

<span lang="EN-US">(this UI is all about creating a dashboard)</span>

<span lang="EN-US"><HABMIN></span>

<span lang="EN-US">(which we already used for inclusion of Z-Wave devices)</span>

</td>

<td width="338" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 253.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image158.jpg)

</td>

</tr>

<tr>

<td width="319" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 239.3pt;">

<span lang="EN-US">You can also install more UIs in</span>

<span lang="EN-US">PAPER UI Add-ons section:</span>

<span lang="EN-US">http://192.168.2.106:8080/paperui/index.html#/extensions</span>

<span lang="EN-US">on the tab <USER INTERFACES></span>

</td>

<td width="338" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 253.4pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image159.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

## <a name="_Toc485150950"><span lang="EN-US">BASIC UI dashboard</span></a>

<span lang="EN-US">Since this is a beginner’s tutorial where I am trying to get things done using as less textual coding as possible, I will not go into the details of creating a dashboard for the BASIC UI since it requires the file based approach.</span>

<span lang="EN-US">Tough you might find that some specific requirements to a dashboard can only be solved creating this textual sitemap configuration and using BASIC UI for displaying your dashboard.</span>

<span lang="EN-US">You can find more information in how to setup and use BASIC UI on:</span>

[<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/configuration/sitemaps.html</span></span>](http://docs.openhab.org/configuration/sitemaps.html)

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-US" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150951"><span lang="EN-US">PAPER UI dashboard</span></a>

<span lang="EN-US">The simplest way of creating an interactive user interface is in just clicking on the <CONTROL> tab to PAPTER UI. Now you should see all the items grouped by the things they belong to.</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image160.jpg)

<span lang="EN-US"> </span>

<span lang="EN-US">You can also easily create different tabs of things by adding <Location> information to the thing in the thing tab:</span>

<span lang="EN-US">NOTE: I had issues in updating a few things, so it will be good to it while creating the things</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image161.jpg)

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

<span lang="EN-US"> </span>

<span lang="EN-US">Now you will have Control panel giving you various tabs with items grouped by their things</span>

<span lang="EN-US">Tab</span> <OUTSIDE>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image162.jpg)

<span lang="EN-US">Standard tab</span> <OTHER>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image163.jpg)

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-US" style='font-size: 13pt; line-height: 115%; font-family: "Calibri Light","sans-serif";'> </span>**

## <a name="_Toc485150952"><span lang="EN-US">HABPANEL UI dashboard</span></a>

<span lang="EN-US">The HABPANEL UI is all about creation a dashboard for your home automation project. Therefore you can not to do all the configuration work for openHAB2 in this UI. The configuration hast to be done in the other UIs</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="310" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 232.2pt;">

<span lang="EN-US">Start HABPANEL</span>

<span lang="EN-US">http://xxx.xxx.xxx.xxx:8080/HABPANEL/index.html#/</span>

<span lang="EN-US">It will come up a complete blank panel asking you to start configuration</span>

</td>

<td width="347" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 260.5pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image164.jpg)

</td>

</tr>

<tr>

<td width="310" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 232.2pt;">

<span lang="EN-US">You now can choose to</span>

<span lang="EN-US"><Add new dashboard></span>

<span lang="EN-US"> </span>

</td>

<td width="347" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 260.5pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image165.png)

</td>

</tr>

<tr>

<td width="310" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 232.2pt;">

<span lang="EN-US" style="color: black;">Create switches to control the Z-Wave switches</span>

<span lang="EN-US" style="color: rgb(91, 155, 213);">Details MISSING</span>

</td>

<td width="347" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 260.5pt;">

![Picture MISSING](openHAB2_Raspberry_beginner-s_walkthrough_files/image166.png)

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

<span lang="EN-US">You can find the standard documentation on:</span>

[<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/addons/uis/HABPANEL/readme.html</span></span>](http://docs.openhab.org/addons/uis/habpanel/readme.html)

## <span lang="EN-US"> </span>

## <a name="_Toc485150953"><span lang="EN-US">HABMIN dashboard</span></a>

<span lang="EN-US">And once again, since this is a beginner’s tutorial I can’t go into all the possibilities of how to create a dashboard in openHAB2\. So I will not go into creating a dashboard in HABMIN. But be aware the HABMIN is providing a powerful graphical way of creating dashboards you might want to have a look at.</span>

<span lang="EN-US">You can find the standard documentation on:</span>

[<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/addons/uis/habmin/readme.html</span></span>](http://docs.openhab.org/addons/uis/habmin/readme.html)

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

# <a name="_Toc485150954"><span lang="EN-US">Chapter 12: Creating rules</span></a>

<span lang="EN-US">Since rules can’t be configured using the PAPER UI (stable version) you now have to go to the text files for now. For this part we will now use the</span> <span lang="EN-GB">Eclipse Smart Home Designer since it creates at least some syntax highlighting.</span>

<span lang="EN-US">REMARK: You might find already some functionality about configuration of rules in the PAPER UI snapshot versions so there will be some changes in the way of doing rules more easily in the future. Also HABmin is providing some kind of graphical rule engine.</span>

## <a name="_Toc485150955"><span lang="EN-GB">Creating the myfirstrule.rules file</span></a>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="231" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">Start</span> <span lang="EN-GB">Eclipse Smart Home Designer on your PC</span>

<span lang="EN-GB">Make sure you have mapped the Raspbian samba drive to your PC and</span> <span lang="EN-US">Start</span> <span lang="EN-GB">Eclipse Smart Home Designer is set to the right folder in this samba drive (see Chapter 7: Installation of Eclipse Smart Home Designer -: part launching first time)</span>

<span lang="EN-GB">You should now the augmented icons for the different folders</span>

<span lang="EN-GB">If you check the Rules folder you will only find a readme.txt file</span>

</td>

<td width="426" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image167.jpg)

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">You need to create a file with the ending .rules to store your rules there.</span>

<span lang="EN-US">The fastest way of doing it is using the basic file management functionality of</span> <span lang="EN-GB">Eclipse Smart Home Designer</span>

<span lang="EN-US">Right click on the readme.txt file and select copy</span>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image168.jpg)

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">Then right click again and select Paste</span>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image169.jpg)

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">A new window will ask you to enter a new file name.</span>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image170.jpg)

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">Change the file name to</span>

<span lang="EN-US">myfirstrule.rules</span>

<span lang="EN-US">an press</span> <OK>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image171.jpg)

myfirstrule.rules

<OK>

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">A new file will appear in the Rules folder showing the rule icon</span>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image172.png)

</td>

</tr>

<tr>

<td width="231" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 173.45pt;">

<span lang="EN-US">Now double click on the file to open it and delete the old content to have a plain rule rile</span>

<span lang="EN-US"> </span>

<span lang="EN-US"> </span>

<span lang="EN-US">And save the rule file again</span>

</td>

<td width="426" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 319.25pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image173.jpg)

<ctrl+a>

<del>

<ctrlss>

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

## <a name="_Toc485150956"><span lang="EN-US">Creating a basic rules</span></a>

<span lang="EN-US">I will try to give some basic rule examples to start with but you have to be aware:</span>

**<span lang="EN-US" style="color: red;">DISCLAIMER:</span>**

**_<span lang="EN-US" style="color: red;">I am no coding expert at all and writing rules is still the most difficult part in my home automation project (finding the right commands, the right syntax and so on), so you might be better off using to other tutorials</span>_**_<span lang="EN-US" style="color: red;">.</span>_

<span lang="EN-US">For the standard rules documentation incl. the rule syntax please refer to the online documentation:</span>

[<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">http://docs.openhab.org/configuration/rules-dsl.html</span></span>](http://docs.openhab.org/configuration/rules-dsl.html)

<span lang="EN-US">You can also find some rules samples on:</span>

[<span class="Heading9Char"><span lang="EN-US" style="font-size: 10pt; line-height: 115%; color: windowtext; text-decoration: none;">https://github.com/openhab/openhab1-addons/wiki/Samples-Rules</span></span>](https://github.com/openhab/openhab1-addons/wiki/Samples-Rules)

<span lang="EN-US"> </span>

<span lang="EN-US">And maybe some coding experts in the community will find the time to create a kind of an openHAB2 compendium to make it easier the non-experts to do rules.</span>

<span lang="EN-US">REMAKR: Yes, I know there are plenty of online documentation sites available, but the problem for me was the “plenty” part of it since I always had to go through plenty different websites to finally get the syntax right and make the rule do, what I wanted it to do.</span>

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

**<span lang="EN-US" style='font-family: "Calibri Light","sans-serif";'> </span>**

### <a name="_Toc485150957"><span lang="EN-US">Basic rule example:</span></a>

<span lang="EN-US">We will use the:</span>

<span lang="EN-US">KeyFob_Gen5</span>

<span lang="EN-US">to control some items linked to</span>

<span lang="EN-US">Z-Wave Node 2: FGS223 Double Switch 2</span>

<span lang="EN-US">Z-Wave Node 3: MSP-3-1-X1 Z-Wave Plus Micro Smart Plug ON/OFF</span>

<span lang="EN-US">Yamaha Receiver RX-V581</span>

<span lang="EN-US">DUMMYTHING_SamsungTV</span>

<span lang="EN-US">HF-LPB100-ZJ200 (WiFi LED)</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="168" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 125.9pt;">

<span lang="EN-US">Just copy the code to the right directly into your myfirstrule.rules file</span>

<span lang="EN-US"> </span>

</td>

<td width="489" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 366.8pt;">

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>rule</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(42, 0, 255);'>"KeyFob"</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>when</span>**

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>Item</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>received update</span>**

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>then</span>**

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 1 - Button 1 (up left) pressed short</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>1</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//<u>Swithing</u> ON the items DoubbleSwitch01_Relais1 and SchuKo01</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DoubbleSwitch01_Relais1</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>SchuKo01</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 2 - Button 1 (up left) pressed long</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>2</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//<u>Swithing</u> OFF the items DoubbleSwitch01_Relais1 and SchuKo01</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DoubbleSwitch01_Relais1</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>SchuKo01</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 3 - Button 2 (up left) pressed short</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>3</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Switching ON the items YamahaReceiverRXV581_Power and DUMMYITEM_SamsungTV_Power   </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>YamahaReceiverRXV581_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DUMMYITEM_SamsungTV_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 4 - Button 2 (up left) pressed long</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>4</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Switching OFF the items YamahaReceiverRXV581_Power and DUMMYITEM_SamsungTV_Power   </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>YamahaReceiverRXV581_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DUMMYITEM_SamsungTV_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)       </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 5 - Button 3 (up left) pressed short</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>5</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Switching ON the item HFLPB100ZJ200_Power</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>HFLPB100ZJ200_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)   </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 6 - Button 3 (up left) pressed long</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>6</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Switching OFF the item HFLPB100ZJ200_Power</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>HFLPB100ZJ200_Power</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)  </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 7 - Button 4 (up left) pressed short</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>7</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//NOTE: since setting the color will influence the dimming of the WHITE</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//          so if you want to set both values at the same time, always</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//          set color first and than</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//      set the dimming of WHITE</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Changing the color of the item HFLPB100ZJ200_Color to RED</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//openHAB2 is requesting the color to be set in HSL code (Hue, Saturation, Lightness" or in openHAB terms "HSBType" (Hue, Saturation, Brightness)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//To convert RGB code to HSL code just go to e.g. http://www.rapidtables.com/convert/color/rgb-to-hsl.htm</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>                  _sendCommand_ (<u>HFLPB100ZJ200_Color</u>,(</span>**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>new</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>HSBType(</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(42, 0, 255);'>"0,100,50"</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)))  </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Dimming the item HFLPB100ZJ200_White to 50%</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>HFLPB100ZJ200_White</u>,</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>50</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>     </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Scene number 8 - Button 4 (up left) pressed long</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>ZWaveNode9ZW0884ButtonKeyfobGen5_SceneNumber</u>.state ==</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>8</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//NOTE: since setting the color will influence the dimming of the WHITE</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//          so if you want to set both values at the same time, always</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//          set color first and than</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//      set the dimming of WHITE</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Changing the color of the item HFLPB100ZJ200_Color to GREEN</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//openHAB2 is requesting the color to be set in HSL code (Hue, Saturation, Lightness" or in openHAB terms "HSBType" (Hue, Saturation, Brightness)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//To convert RGB code to HSL code just go to e.g. http://www.rapidtables.com/convert/color/rgb-to-hsl.htm</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>                  _sendCommand_ (<u>HFLPB100ZJ200_Color</u>,(</span>**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>new</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>HSBType(</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(42, 0, 255);'>"120,100,50"</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)))</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>//Dimming the item HFLPB100ZJ200_White to 100%</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> _<span style='font-size: 10pt; font-family: "Courier New"; color: black;'>sendCommand</span>_ <span style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>HFLPB100ZJ200_White</u>,</span> <span style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>100</span><span style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

**<span style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>end</span>**<span style='font-size: 10pt; font-family: "Courier New"; color: black;'>  </span>

</td>

</tr>

<tr>

<td width="168" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 125.9pt;">

<span lang="EN-US">Save the rule file.</span>

<span lang="EN-US">The rule should now be available</span>

</td>

<td width="489" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 366.8pt;">

<span lang="EN-US"><crtl+s></span>

</td>

</tr>

</tbody>

</table>

<span lang="EN-US">Test it by clicking through the buttons (pressed long and pressed short)  
</span>

## <a name="_Toc485150958"><span lang="EN-US">Basic tips for debugging rules</span></a>

### <a name="_Toc485150959"><span lang="EN-US">Creating an item the see the value of a variable of a rule online</span></a>

<span lang="EN-US">The standard way of debugging a rule would be to use a logfile.</span>

<span lang="EN-US">For simple problems you might also be able to visualize the variables online by creation item with the same type and posting the value of the variable inside the rule</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="368" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">If you are using a variable in your rule initially set to</span>

</td>

<td width="289" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

var Number loop_counter = 0

<span lang="EN-GB"> </span>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Create the item</span> <span lang="EN-US">Counter_Item</span> <span lang="EN-GB">with the same type:</span>

<span lang="EN-GB">In PAPER UI switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Items</span>

<span lang="EN-US">And press the blue icon (+)</span>

<span lang="EN-US">Enter Name Counter_Item</span>

<span lang="EN-US">Select Typ</span> <Number>

<span lang="EN-US">And confirm the creation by clicking again on the blue icon (+)</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image174.jpg)

<span lang="EN-US">Counter_Item</span>

<Number>

<(+)>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Result:</span>

<span lang="EN-GB">A new item called</span> <span lang="EN-US">Counter_Item</span>

<span lang="EN-GB">should be visible in the item tab</span>

<span lang="EN-GB">NOTE: Since this Item is not linked to a thing it will not show up in the</span> <Control> <span lang="EN-GB">Tab to PAPER UI.</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image175.jpg)

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Now enter a line into your rule to post the value of the</span> var <span lang="EN-GB">to the</span> <span lang="EN-US">Counter_Item</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

postUpdate(Counter_Item, loop_counter)

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">To show the value on a dashboard you have to use e.g. HABPANEL</span>

<span lang="EN-US">Start HABPANEL</span>

http://xxx.xxx.xxx.xxx:8080/HABPANEL/index.html#/

<span lang="EN-GB">and select</span> <Edit dashboards> <span lang="EN-GB">in the upper right corner</span>

then <Add new dashboard>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">enter the name</span> Debug <span lang="EN-GB">and</span> <OK>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image176.png)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image177.jpg)

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image178.jpg)

Debug

<OK>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Now you should have the dashboard</span> <Debug> <span lang="EN-GB">available in your HABPANEL</span>

<span lang="EN-GB">Select the dashboard</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image179.jpg)

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">If you now hover with your mouse right of the dashboard name the</span> <span lang="EN-US"><Edit _Debug_></span> <span lang="EN-GB">icon will appear.</span>

<span lang="EN-GB">Click on it to enter the edit mode.</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image180.png)

<Edit _Debug_>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">The edit mode is indicated by the two icons</span> <Save> <span lang="EN-GB">and</span> <Run>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image181.png)

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Now you have to</span> <+ Add Widget>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">You have to use the</span> <Dummy> <span lang="EN-GB">widget to display numbers</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image182.jpg)

<+ Add Widget>

<Dummy>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">The new Widget will appear on your dashboard</span>

<span lang="EN-GB">NOTE: you can easily change the size of the widget by dragging the lower right corner. I will snap to a predefined grid</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image183.jpg) 

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">To edit the widget you have to click on the 3 dots in the upper right corner of the widget and select</span> <Edit>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image184.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image185.jpg)

<.>

<Edit>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">In this window you can change the name to</span> Counter Item Debug

<span lang="EN-GB">You have to select the</span> <span lang="EN-US">openHAB item</span> <span lang="EN-US"></span> <Counter_Item> <span lang="EN-GB">to link it to this widget.</span>

<span lang="EN-GB">Optional you can change font size, add a unit and format or add some icons.</span>

<span lang="EN-GB">Now</span> <Save> <span lang="EN-GB">the widget.</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image186.jpg)

Counter Item Debug

<Counter_Item>

<Save>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">Now</span> <Save> <span lang="EN-GB">the dashboard and</span> <Run> <span lang="EN-GB">it.</span>

<span lang="EN-GB"> </span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image187.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image188.jpg)

<Save>

<Run>

</td>

</tr>

<tr>

<td width="368" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 276.05pt;">

<span lang="EN-GB">You will now see the value of your rule variable displayed dynamically on your HABPANEL dashboard</span>

</td>

<td width="289" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 216.65pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image189.jpg)

</td>

</tr>

</tbody>

</table>

**<span lang="EN-US" style='font-size: 11pt; line-height: 112%; font-family: "Calibri Light","sans-serif";'>  
</span>**

### <a name="_Toc485150960"><span lang="EN-US">Creating a virtual switch on HABPANEL to use it in a rule</span></a>

<span lang="EN-US">This switch might come handy if you are debugging your rule while physically having no access to the switch. Standing up and running to the switch might do you some good when it comes down to fitness but surely is disturbing while developing your rule</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="376" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Create the item</span> <span lang="EN-US">Dummy_Switch</span> <span lang="EN-GB">with the same type:</span>

<span lang="EN-GB">In PAPER UI switch to</span>

<span lang="EN-GB">-Configuration</span>

<span lang="EN-GB">--Items</span>

<span lang="EN-US">And press the blue icon (+)</span>

<span lang="EN-US">Enter Name Dummy_Switch</span>

<span lang="EN-US">Select Typ</span> <Switch>

<span lang="EN-US">And confirm the creation by clicking again on the blue icon (+)</span>

</td>

<td width="281" valign="top" style="border-style: solid solid solid none; border-color: windowtext windowtext windowtext -moz-use-text-color; border-width: 1pt 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image190.jpg)

<span lang="EN-US">Dummy_Switch</span>

<Switch>

<(+)>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Result:</span>

<span lang="EN-GB">A new item called</span> <span lang="EN-US">Dummy_Switch</span>

<span lang="EN-GB">should be visible in the item tab</span>

<span lang="EN-GB">NOTE: Since this Item is not linked to a thing it will not show up in the</span> <Control> <span lang="EN-GB">Tab to PAPER UI.</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image191.jpg)

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Now replace the item name of the</span> _physical_switch_ <span lang="EN-GB">with the name of the</span> <span lang="EN-US">Dummy_Switch</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

_physical_switch_

<span lang="EN-US">will become Dummy_Switch</span>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">To use the</span> <span lang="EN-US">Dummy_Switch</span> <span lang="EN-GB">on a dashboard you have to use e.g. HABPANEL</span>

<span lang="EN-US">Start HABPANEL</span>

http://xxx.xxx.xxx.xxx:8080/HABPANEL/index.html#/

<span lang="EN-GB">and select</span> <Edit dashboards> <span lang="EN-GB">in the upper right corner</span>

then <Add new dashboard>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">enter the name</span> Debug <span lang="EN-GB">and</span> <OK>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image176.png)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image192.jpg)

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image193.jpg)

Debug

<OK>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Now you should have the dashboard</span> <Debug> <span lang="EN-GB">available in your HABPANEL</span>

<span lang="EN-GB">Select the dashboard</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image179.jpg)

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">If you now hover with your mouse right of the dashboard name the</span> <span lang="EN-US"><Edit _Debug_></span> <span lang="EN-GB">icon will appear.</span>

<span lang="EN-GB">Click on it to enter the edit mode.</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image180.png)

<Edit _Debug_>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">The edit mode is indicated by the two icons</span> <Save> <span lang="EN-GB">and</span> <Run>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image181.png)

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Now you have to</span> <+ Add Widget>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB"> </span>

<span lang="EN-GB">You have to use the</span> <Button> <span lang="EN-GB">widget to display numbers</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image194.jpg)

<+ Add Widget>

<Button>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">The new Widget will appear on your dashboard</span>

<span lang="EN-GB">NOTE: you can easily change the size of the widget by dragging the lower right corner. I will snap to a predefined grid</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image183.jpg) 

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">To edit the widget you have to click on the 3 dots in the upper right corner of the widget and select</span> <Edit>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image184.jpg)![](openHAB2_Raspberry_beginner-s_walkthrough_files/image185.jpg)

<.>

<Edit>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">In this window you can change the name to</span> Dummy Switch ON/OFF

<span lang="EN-GB">You have to select the</span> <span lang="EN-US">openHAB item</span> <span lang="EN-US"></span> <Dummy_Switch> <span lang="EN-GB">to link it to this widget.</span>

<span lang="EN-GB">Optional you can select display options and icons</span>

<span lang="EN-GB">Now</span> <Save> <span lang="EN-GB">the widget.</span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image195.jpg)

Dummy Switch ON/OFF

<Dummy_Switch>

<Save>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">Now</span> <Save> <span lang="EN-GB">the dashboard and</span> <Run> <span lang="EN-GB">it.</span>

<span lang="EN-GB"> </span>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image196.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image197.jpg)

<Save>

<Run>

</td>

</tr>

<tr>

<td width="376" valign="top" style="border-style: none solid solid; border-color: -moz-use-text-color windowtext windowtext; border-width: medium 1pt 1pt; padding: 0cm 5.4pt; width: 281.7pt;">

<span lang="EN-GB">You will now see the</span> Dummy_Switch <span lang="EN-GB">Item be visualized by the</span> Dummy Switch ON/OFF <span lang="EN-GB">widget.</span>

<span lang="EN-GB">The initial state should be</span> <Inactive>

<span lang="EN-US">Just click on the widget to change the state to</span> <span lang="EN-US"></span> <Active>

</td>

<td width="281" valign="top" style="border-style: none solid solid none; border-color: -moz-use-text-color windowtext windowtext -moz-use-text-color; border-width: medium 1pt 1pt medium; padding: 0cm 5.4pt; width: 211pt;">

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image198.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image199.jpg)

</td>

</tr>

</tbody>

</table>

<span lang="EN-US"> </span>

<span lang="EN-US" style='font-size: 11pt; line-height: 115%; font-family: "Calibri","sans-serif";'>  
</span>

<span lang="EN-US"> </span>

## <a name="_Toc485150961"><span lang="EN-US">Further Rule examples based on this home automation project:</span></a>

### <a name="_Toc485150962"><span lang="EN-US">Switching ON/OFF switches based on luminance reading of the multisensory</span></a>

<span lang="EN-US">The rule is designed to switch on/off the Z-Wave Node 2: FGS223 Double Switch 2 based on the</span> illumination measured by the <span lang="EN-US">Z-Wave Node 6: ZW100 MultiSensor 6</span>

<span lang="EN-US">The trigger value is set to 10 LUX</span>

<span lang="EN-US">To prevent von switching on/off if the illumination is around 10 lumen and e.g. just a cloud is casting a temporarily shadow, there is a counter included which is measuring multiple times the illumination and only allows to triggering the switch if there reading is consistently (10 times) above or below the trigger value.</span>

<span lang="EN-US">NOTE: Make sure you have create the item Counter_Item since it’s used in the rule (see: part “Creating an item the see the value of a variable of a rule online” in this chapter).</span>

<span lang="EN-US">REMARK: This was done as some kind of coding and configuring HABPANEL exercise. You might get the same result in just checking the reading in a less frequent period, forget about the counter and just trigger the switch when the illumination reading is above or below the trigger value.</span>

<span lang="EN-US">You can also use this Counter_Item to display some tendency whether your light is about to switch ON/OFF depending on the value of the Counter_Item on your dashboard. So if you play a little with the “knob” widget in HABPANEL it might look like this:</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image200.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image201.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image202.jpg) ![](openHAB2_Raspberry_beginner-s_walkthrough_files/image203.jpg)

<span lang="EN-US">Then you add some other readings of your multissor, the wattage reading and trigger of your switch, a clock widget and you have a complete dashboard of your real weather and let it trigger your outside ligth.</span>

![](openHAB2_Raspberry_beginner-s_walkthrough_files/image204.jpg)<span lang="EN-US">  
</span>

<span lang="EN-US">You can just add these lines at the bottom of your existing rule file or create a new file in the same folder</span>

<table class="MsoTableGrid" style="border: medium none ; border-collapse: collapse;" border="1" cellspacing="0" cellpadding="0">

<tbody>

<tr>

<td width="652" valign="top" style="border: 1pt solid windowtext; padding: 0cm 5.4pt; width: 488.9pt;">

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>var</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>Number loop_counter =</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>0</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>rule</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(42, 0, 255);'>"check_illumination"</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// using the loop_counter to ensure that it is</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// 10 times in a row darker/lighter before triggering switch</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New";'> </span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>when</span>**

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// every x seconds "0/x" the value is checked</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// 0/30 means every 30 <u>sec</u> the value is checked</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>Time</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>cron</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(42, 0, 255);'>"0/30 * * ? * * *"</span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>then</span>**

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// reset loop_counter if required (counter outside -5 +5 range)</span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>>= -</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>5</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>&&</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'><=</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>5</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>){</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(63, 127, 95);'>// <= 10 is defining the LUX trigger value when <u>ligth</u> is <u>swiched</u> ON/OFF</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>MultiSens_Helligkeit</u>.state <=</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>10</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>> -</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>5</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>=</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>-</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>1</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_postUpdate_(<u>Counter_Item</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>else</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>{</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>DoubbleSwitch01_Relais1</u>.state ==</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DoubbleSwitch01_Relais1</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>      }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>else</span>**

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'><</span> <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>5</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>) {</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>=</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>+</span><span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>1</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_postUpdate_(<u>Counter_Item</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>else</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>{</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> **<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>if</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>(<u>DoubbleSwitch01_Relais1</u>.state ==</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>ON</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>_sendCommand_ (<u>DoubbleSwitch01_Relais1</u>,</span> _<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>OFF</span>_<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>)</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

**<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>else</span>** <span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'>{</span>

<span lang="EN-US" style='font-size: 10pt; font-family: "Courier New"; color: black;'></span> _<span style='font-size: 10pt; font-family: "Courier New"; color: rgb(0, 0, 192);'>loop_counter</span>_ <span style='font-size: 10pt; font-family: "Courier New"; color: black;'>=</span> <span style='font-size: 10pt; font-family: "Courier New"; color: rgb(125, 125, 125);'>0</span>

<span style='font-size: 10pt; font-family: "Courier New"; color: black;'>            }</span>

**<span style='font-size: 10pt; font-family: "Courier New"; color: rgb(127, 0, 85);'>end</span>**

</td>

</tr>

</tbody>

</table>

<span lang="EN-US">And save the file</span>

<span lang="EN-US"> </span>
 
</div>

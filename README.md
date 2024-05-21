# Pi-Hole-on-raspberry-pie

Pi-hole is a Linux network-level advertisement and Internet tracker blocking application which acts as a DNS sinkhole and optionally a DHCP server, intended for use on a private network. It is designed for low-power embedded devices with network capability, such as the Raspberry Pi, but can be installed on almost any Linux machine.

Pi-hole has the ability to block traditional website advertisements as well as advertisements in unconventional places, such as smart TVs and mobile operating system advertisements.

<h3> <b>* Requrmerts</b> </h3>

  Raspberry with microSD card
  Cpomputer to configer the microSD card.

  Download the SD card formenter and Raspberry Pi imager

 After installing Imager, run rpi-imager or click the Raspberry Pi Imager icon to open the program.

 ![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/e112d26b-d1d3-4938-bab1-6c0659533458)

 Click Choose device and select your Raspberry Pi model from the list.

 ![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/8401c5d1-380d-414b-bc08-2380fea38740)

 After that, click Choose OS to pick an installation operating system. The Raspberry Pi OS version that Imager recommends for your model is always displayed first in the list.st.

 ![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/79e2b98e-3ca2-4f89-936a-9b63e149d54d)

 Link your computer to the storage device of your choice. For instance, use an external or integrated SD card reader to insert a microSD card. Next, choose your storage device by clicking Choose storage.

 ![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/8c1ba304-c1a1-405b-ba49-3a1cf0493cbc)

 click Next.

 ![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/74a5b9a7-676c-419d-bed0-f6ff60deec45)

 Imager will prompt you to apply OS customization in a popup. Setting up your Raspberry Pi through the OS customization settings is highly advised. To access the OS customization, click the Edit Settings icon.

Should you choose not to customize your Raspberry Pi through the OS customization options, Raspberry Pi OS will prompt you for the same data during the configuration wizard's initial boot. If you would like to forego OS customization, choose the No box.

<h3> <b> customization of the OS </b> </h3>

Prior to initial startup, you can configure your Raspberry Pi using the OS customization menu. It is possible to preconfigure:

   * a username and password

   * Wi-Fi credentials

   * the device hostname

   * the time zone

   * your keyboard layout

   * remote connectivity

You may encounter a prompt asking for authorization to load Wi-Fi credentials from your host computer when you initially access the OS customization menu. Imager will prefill your Wi-Fi credentials from the network you are presently connected to if you answer "yes." You can manually enter your Wi-Fi credentials if you answer "no."

The hostname setting establishes the hostname that your Raspberry Pi uses for mDNS broadcasts to the network. Using <hostname>.local or <hostname>.lan, other networked devices can connect to your Raspberry Pi and communicate with your computer.

On your Raspberry Pi, the admin user account's username and password are specified using the username and password option.

You can set your wireless network's password and SSID (name) by selecting the wireless LAN option. You should activate the "Hidden SSID" feature if your network does not broadcast an SSID publicly. Imager sets the "Wireless LAN country" to your current location by default. The Wi-Fi broadcast frequencies that your Raspberry Pi uses are managed by this parameter. If you intend to use a headless Raspberry Pi, enter the login credentials for the wireless LAN option.

You can specify your Pi's time zone and preferred keyboard layout using the locale settings option.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/61bb2d71-848c-46c5-9fe9-6d33066ac10e)

You can configure the Services tab to enable remote Raspberry Pi connections.

Select the Enable SSH option if you intend to use your Raspberry Pi remotely across your network. In case you intend to use a headless Raspberry Pi, you ought to activate this feature.

To SSH onto your Raspberry Pi via a network, select the password authentication option and enter the username and password you entered in the general page of OS customization.

To set up your Raspberry Pi for passwordless public-key SSH authentication using a private key from the machine you are presently using, select Allow public-key authentication only. Imager uses the public key that you already have if you have an RSA key set up for SSH. If not, you can create a public/private key pair by clicking Run SSH-keygen. The freshly generated public key will be used by Imager.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/70e65272-9ffd-4324-80b4-88b8cd304abd)

Additionally, an Options menu that lets you adjust Imager's behavior during a write is part of the OS customization. With these options, you can turn off telemetry, automatically unmount storage media after image verification, and play a noise when Imager finishes validating an image.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/2a3272d0-c8ae-4e6d-82d7-c8140e54dc47)

<h3> <b> Write </b> </h3>

Click Save to save your customization when you've completed inputting the OS customization settings.

After that, when you write the image to the storage device, select Yes to apply the OS customization options.

To finally start writing data to the storage device, answer "Yes" when prompted by the "Are you sure you want to continue?" box.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/945a3a02-29fe-4518-8871-dbf4ce99bc47)

The "Write Successful" window indicates that the image has been fully written and validated. Now that the storage device is ready, you can boot a Raspberry Pi from it!

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/8670f6e8-e9bb-4911-920f-93d760776b93)

<h3> <b> Configure the Raspberry Pi. </b> </h3>

Once the operating system image has been installed, attach your storage device to your Raspberry Pi.

To make sure the Raspberry Pi is powered off while you connect peripherals, first unplug the power supply. You can now insert the microSD card that you used to install the operating system into the Raspberry Pi's card slot. You can now attach any additional storage device that you have installed the operating system on to your Raspberry Pi.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/b1976ddc-b32b-484a-9c32-da934be6f89b)

After that, connect any additional devices, such your keyboard, mouse, and monitor.


<h3> <b> starting boot configuration </b> </h3>

Congratulations if you preconfigured your Raspberry Pi using OS modification in Imager! You can use your device now. To find out how to make the most of your Raspberry Pi, continue to the next stages.

Examine the status LED if your Raspberry Pi doesn't boot up in five minutes. See the LED warning flash codes for more details if it's flashing. If your Pi won't start up, try these troubleshooting steps:

 * If you didn't use an SD card as your boot device, try using one now.

 * Reimage your SD card, making sure to finish Imager's verification process in its entirety.

 * Reimage your SD card after updating your Raspberry Pi's bootloader

Upon initial boot, a configuration wizard will be launched on your Raspberry Pi if you decided not to customize the OS using Imager. To utilize the wizard, you'll need a keyboard and monitor; a mouse is not necessary.

customize the OS as per your needs.

<h3> <b> Recommended software  </b> </h3>

Numerous necessary apps are pre-installed on Raspberry Pi OS so you may use them right away. To access additional applications that we believe you'll find helpful, click the raspberry icon located in the upper left corner of the screen. To access the package manager, select Preferences > Recommended Software from the drop-down menu. Many pieces of recommended software are available for free installation here.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/7eb89f97-54b6-41e7-8b58-23da994297b2)

Now open the terminal in admin mode and run the commend blow.

<b> " curl -sSL https://install.pi-hole.net | bash " </b>

This will fire off the installation wizard. When the screen below appears, press ENTER (OK).

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/31fda241-c92a-4eae-be27-182aa4fb9bfb)

The next screen recommends that you DONATE to help the Pi-hole project – I recommend it as well! Press ENTER (OK).

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/607e491e-ee63-445d-bfeb-4d7c91d953a0)

Next, the wizard gives us a warning about using a static IP address – we’ve already covered this, to move the cursor over to Continue and press ENTER.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/5e0b180d-021f-47e2-95b6-ea8bd1d99771)

On this screen, double-check that the IP address shown is the IP address that you want to use for the Pi-hole and then press ENTER (select Yes – Set static IP using current values).

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/1300751f-8e32-4c51-adc8-92f5b216bd51)

Now we are going to pick an upstream DNS provider. This is the DNS server that the Pi-hole will use to do DNS lookups (initial lookups – then they get cached). Since we’re going to be installing Unbound, we’ll be making our own DNS lookups to the primary root domain servers on the Internet, so for now, it’s fine to pick any one of these – I’ll be using Cloudflare (1.1.1.1) for this tutorial.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/b88203b6-e68d-4706-8bb3-3d360d963b4a)

Next we’re asked if we want to use the default included block list – this block list is a list of domains that Pi-hole is going to block for us. This list is perfectly fine, and will block a significant chunk of suspect sites – however, there are many block lists available, and you’ll likely want to add some more – we’ll cover this later in the tutorial. Choose YES and press ENTER.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/47047874-c94d-456b-b16c-3ad0acc49f49)

Next we’re asked if we want to install the Admin Web Interface, which of course we do! Select YES and press ENTER.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/20ede9ea-a2df-4534-a02b-d53f914f38b0)

Another notice about the web server – just choose YES and press ENTER.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/208b2315-a88b-40fc-b1dc-11c7c8d2dd96)

Next, we’re asked if we want to enable query logging. Typically, you will want to say Yes here, but if you’re super security conscious and you don’t want any of your DNS lookups logged, you can also choose No.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/0fc6540b-4e63-45ad-8fec-bcf04ecc3b00)

Now we’re asked about the level of privacy – you can visit the website listed for more information. For this tutorial, we’re going to select ‘Show everything’ and press Continue.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/b06589ab-33c5-4eb1-9fb9-c5068c856fda)

That’s it! After this step, Pi-hole has all of the information it needs to get started. You’ll see it run through a bunch of scripts in the CLI (takes about 2 minutes), and will eventually be brought to this screen:

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/3798beb3-523a-4df2-8451-0571e66304a3)

This last screen provides us with an overview of our installation and displays our password for the admin webpage login. This is not something you should write down because we'll be changing the password in the following step.

The Pi-hole Web GUI Admin Password can be changed.
Run the following command to create a strong password for the Pi-hole admin GUI:
<b> " pihole -a -p " </b>
This will have you input a password and then confirm it.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/cfc8a83b-ac83-4bf5-b90b-99210f2448bb)

Log into the Pi-hole GUI
We’re now ready to log into the GUI for the first time! Open up a browser and input the IP address followed by /admin in this format:

http://xxx.xxx.xxx.xxx/admin

(Substitute my IP address with your own). Note also that this is HTTP and not HTTPS.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/4bd11d0b-baa1-424b-a8c4-267ae6ede2e5)

Enter the Admin password that you set in the previous step and click ‘Log in.’ Upon logging in, we’re presented with the Pi-hole Dashboard – let’s take a look around!

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/4a90d9db-6e25-43e3-be1f-c04513a51871)

Since we haven't used this Pi-hole yet, we don't have a ton of meaningful data.they will begin to appear as soon as we begin sending DNS queries to this server.

Our menu choices are located along the dashboard's left side. Some statistics are shown in the four colored blocks at the top. The total number of requests that Pi-hole has answered is shown in the blue box. The number of those queries that matched FQDNs on the block list and were blocked is indicated by the red box. The percentage of blocked requests is represented by the yellow box (red box divided into the blue box). The number of domains that are on the block lists is finally shown in the green box. Since we now only have one block list, we can see that this Pi-hole will block roughly 158,000 domains.

The Pi-hole's DNS lookup history is displayed in descending order in the Query Log, with the most recent lookups at the top. All domain statuses, including blocked and passed domains, are visible. There is a button to whitelist prohibited domains and a button to blacklist passed domains.

Long-Term Data: Similar to the Query Log, this part allows you to go down into the DNS history of the Pi-hole and perform fine-grained filtering on the data.

Groups and Clients: This section has some fairly fascinating capabilities that we won't delve into for the sake of this tutorial, but you can use it to block DNS queries for all devices with the exception of those in a certain group. Alternatively, you can also go more specific about which clients and groups utilize which block lists if you wanted to ONLY prevent DNS queries for devices in a particular group.

<a href="https://avoidthehack.com/best-pihole-blocklists"> The Best Pi-hole Blocklists </a> – Avoidthehack.com – This article does an excellent job of explaining the different types of block lists, and then lists a number of resources for lists in different categories of blocking.

Adlists: By default, we have a well-maintained default block list that blocks a large number of websites without impairing standard Internet functioning. However, bear in mind that the more sites you add to your block lists, the higher the likelihood that you will break something. That being said, you can be VERY specific about what you're blocking, including malicious websites, adult content, ad sites, tracking & telemetry sites, and more. Specific public block lists exist for each of these types of content. After that, you'll have to deal with your relatives' complaints about "the Internet" not functioning. The secret is to strike a happy balance where a lot of blocking is accomplished without degrading user experience.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/13dd05b4-5b04-4bd7-91dd-2a48500eea79)

I'm going to copy and paste the first two green URLs from each Firebog section for this lesson. Feel free to repeat this process for as many block lists as you like. After finishing, we must instruct Pi-hole to import these lists.

Navigate to Tools –> Update Gravity and then click the ‘Update’ button. This will comb through all of the block lists and add the blocked URLs to the Pi-hole database. Once complete, you’ll see a green ‘Success’ banner at the top of the screen.

![image](https://github.com/patel5d2/Pi-Hole-on-raspberry-pie/assets/131821512/e99d3c83-ad91-47d4-8377-b56878352efc)

Congratulations you have successfully started blocking the website. That you don't want in your network and it is across the network level locker so once you configure it here, router all of your device going to block those websites.

I have also made two custom block list one for mix and match and one for YouTube, which I wanted to do eagerly feel free to use that as well.

As a last resort, you can manually set each device to use Pi-hole as its DNS server.

For more assistant please follow the official guideline on here : https://docs.pi-hole.net/main/basic-install/





















  
  
  

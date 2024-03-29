# **Samsung G9-Compatible KVM Switch**

## **Purpose**
The goal of this project is to design a KVM switch with a combination of features that, to my knowledge, does not yet exist. After hours of research and purchasing several different KVMs, there wasn't a single KVM that met the requirements of my current home-office setup. The following paragraphs will describe the current home-office hardware and the relevant technical specifications.

This repo will serve as a means to collect my thoughts, research, and knowledge on the multitude of technologies that comprise the modern-day KVM switch. It will also be the home of the future design of said KVM switch.

## **Repository Structure**
| Directory | Description |
| --------- | ----------- |
| [Block Diagrams](https://github.com/aflyingcougar/G9-Compatible-KVM-Switch/tree/master/Block%20Diagrams) | Conceptual diagrams to aid with preliminary design |
| [Datasheets](https://github.com/aflyingcougar/G9-Compatible-KVM-Switch/tree/master/Datasheets) | PDFs datasheets for all design components |
| [Design](https://github.com/aflyingcougar/G9-Compatible-KVM-Switch/tree/master/Design) | Place to store all engineering project folders (ECAD) |
| [Documentation](https://github.com/aflyingcougar/G9-Compatible-KVM-Switch/tree/master/Documentation) | Contains all generated documentation for the KVM switch design |
| [Reference](https://github.com/aflyingcougar/G9-Compatible-KVM-Switch/tree/master/Reference) | Reference guides, industry standards, etc. |

## **Home-Office Hardware**
- Monitor
	- Samsung Odyssey G9
		- Target Resolution: 5120x1440
		- Target Refresh Rate: 120 Hz
		- DisplayPort 1.4 (HBR3)
- Computers
	- Gaming Desktop
		- Windows 10/11
		- RTX 3080 (DisplayPort 1.4a)
		- 4 x USB 3.2 Gen 2 ports (10 Gb/s)

	- MacBook Pro (16-inch, 2019, 2.6 GHz)
		- 4 x Thunderbolt 3 (USB-C) ports
			- Charging (96W USB-C Power Adapter)
			- DisplayPort ??
			- USB 3.1 Gen 2 (10 Gb/s)

	- Peripherals
		- USB Keyboard
		- USB Mouse

### **Notes**
- When using a USB-C to DisplayPort cable, MacBook Pro is confirmed to negotiate 5120x1440 @ 120 Hz!
	- Does the MBP use Thunderbolt controller when operating at 5120x1440 @ 120 Hz?
		- System report contains the following line under Hardware > Graphics/Displays: *Connection Type: Thunderbolt/DisplayPort*
		- System report shows USB 3.1 bus 5 Gb/s link to Targus Dock (DisplayLink)
		- **Haven't found documented proof, but empirical results seem to indicate that the MBP is indeed capable of TB3 with USB4 and DP 1.4 at 5120x1440 @ 120Hz.**
			

## **Minimum Desired Features**
1. Single-cable solution for connecting to MacBook Pro (Thunderbolt 3)
2. Minimum 120Hz support for Gaming Desktop
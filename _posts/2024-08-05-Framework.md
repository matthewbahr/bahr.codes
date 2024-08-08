---
layout: post
title: "A frame.work cassette player"
date: 2024-08-05
---

# The Deck

However I've been fairly unimpressed with a lot of the modern cyberdeck movement - they're consistently pretty but rarely powerful enough to be interesting. A R.Pi 3 or 4 is a powerful little machine for its price and size but it's no replacement for a laptop when it comes to computationally intensive things, be they games or code compilation. 

So I set out on the journey looking at 3 key goals:

1. It had to be a useable machine with power comparable to a laptop
2. It had to fit the retro aesthetic. Being a perfect recreation of what was described in Neuromancer or Snow Crash was less important than it being a computer I would be willing to use in public, in street clothes, in front of others.
3. It had to have a usable screen. None of these 5" or 7" postage stamps - I needed readable text and 1080p.

And without further ado - I present the fruit of my labors, the Hitachi TRQ220 ~~tape recorder~~ Cyberdeck.

## Some design highlights:  

* Powers on by pressing the record button 
* Fan exhaust through mesh grill on the side (originally the aux out)
* Fan intake through the speaker grill on top
* 2x USB-C 3.1 ports accessible - Primarily for video out and charging
* Bluetooth and Wifi 
* An intel i7-1165G7 mobo
* A 55Wh battery 
* 16gb of 3200 DDR4 ram
* 1Tb M.2 NVME drive

## Woes

Like any first iteration - there's a lot of smoke and mirrors that go into keeping this clean on the outside. Inside there's a mess of amateur solder connecting core components like the power button, botched 3d designs that resulted in flush cutter "patches" to the structural components, all of it friction welded using a dremel and some excess PLA. 

## Record to Power

The power button was a devil to get working right. Initially I purchased a pcb with the correct pin outs already set up to control the mobo directly but had a minor speed bump - I bumped it while it was soldered and ripped the traces out. I'm nowhere near good enough to repair such a mistake: so I went back to the original vendor and placed an order for 3 more. After 2 months of silence from the vendor I reached out to Tindie and got a refund for my order: There was no way around it now, I would have to figure out the pinout myself. 

Hesitant to stretch myself even further I resisted the urge to learn PCB design and just bought the correct connector for the header, figured out which pins I meeded to bridge, and then soldered them to a circuit that the power button would complete. It only took 3 weeks to get that right! 

After getting the header figured out I connected it up to the record button by running hook up wire to the lever arm that moved the original internals and a second wire that is placed so that the pressing of the record button touches the exposed wire, completing the circuit. Simple and straightforward!

## Wifi card 

Thew only part of the framework mainboard that didn't fit in the guts of the casette player was the wifi card which was inserted via a M2 pcie slot. I looked for risers that might have been able to do a sharp 90° bend to get the card inside - to no avail. i had less than a centemeter to perform a 180 and attach the card.

It wasn't really an option to run without it: Even if I didn't need wifi I _did_ need bluetooth. 

The only option wad to cut through the case and print a cover for it. This was particularly nerve wracking because one misstep and I could end up with a botched case. Since it's vintage there's no guarantee of my finding a replacement. 

Ultimately I needn't have worried: the cut went easily. 

## Battery sandwich

The only way I could possibly power this beast was to fit the battery into the same frame. The battery is the same width as the mainboard so I had an easy enough time fitting it into the case. I used cad to carefully align the connector and then twisted the cable 180° to have it connect underneath itself. This remains the sketchiest part of this whole build.

## Field testing 

The ultimate field test was use during my commute on the NYC subway. I decided on something easy to try: Vampire Survivors is a game that can be played with a 2 inputs: a joystick and a single button. I connected up a JoyCon via bluetooth and off I went. It mostly went well too - The ride there was no issue, the ride back however I struggled to get the JoyCon to reconnect. When I got home and took it all apart I found that the wifi card had come disconnected from its antennae - meaning the bluetooth was disconnected as well. I ran another test trying to see if I had just not secured the connectors well enough: same issue. 

The only other option was to solder the connectors onto the wifi card directly. I didnt love this choice but saw no other way. I connected them up with some detaching connectors so it could still be pulled apart... and success! I could go to and from work with the deck on and running.

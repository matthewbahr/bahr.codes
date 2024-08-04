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

## Wifi card 

## Battery sandwich

## Field testing 

## Soldering the wifi card after field tests

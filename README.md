# swift-TCOD 

(c) 2020 Max Goren via/ MIT License (see LICENSE)

Whats Here:

a wrapper for calling functions from the Doryen Library (libtcod) natively in Swift 4.2

this wrapper was developed using:
libtcod version 1.16 alpha 
macOS 10.13.6
XCode 10.1
Swift 4.2


Getting started:

add to your project:
TCOD-wrapper.swift        -contains classes to call from your main.swift to use the functions and types available in libtcod
TCOD-bridging-header.h    -tells Xcode to look in the libtcod headerfiles through its object-c bridge.

other requirements: libtcod - available at https://github.com/libtcod/libtcod
                               
How to use:

import Foundation

let title = "my swift tcod project"
let tcod = TCOD()

let width: Int32 = 80
let height: Int32 = 50
tcod.initRoot(w: width, h: height, title: title)
tcod.clearConsole()

tcod.flush()

while ( !tcod.windowisClosed() ) {

    if (tcod.chkKeypress()) {
    
       tcod.printStr(x: 5, y: 5, str: "Hello, World!")
       
    }  
    
    tcod.flush()

}

tcod.quit()
exit(0)

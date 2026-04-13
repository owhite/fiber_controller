# fiber_controller

### **Collision protection**

* ### Raytools BM110/BM111 "Collision Protection" Kit

* BM111 have a specific internal magnetic sensor and a sacrificial ceramic assembly, but Raytools also offers an external 3D collision mount for high-end machines.  
* [Raytools TRA Nozzle Assembly](https://raytools.vn/product/raytools-original-tra-nozzle-assembly-for-bm111-bm110-laser-cutting-head/)  
* [Raytools 3d head sensor](https://www.amazon.com/Raytools-Head-Capacitive-Sensor-Connector/dp/B0FQ5VNJ7H?th=1) 
* Sacrificial Ceramic Rings If a full magnetic mount is too bulky for your Z-axis design, you should rely on the ceramic ring. For 1.5kW, this is the standard point of failure. [Original Raytools Ceramic Rings (AliExpress)](https://www.aliexpress.com/i/4000780398952.html)

FreeMascot 1064nm Safety Glasses

### **LinuxCNC stack**

* [QtPlasmaC](https://linuxcnc.org/docs/html/plasma/qtplasmac.html)  
* Mesa [7i96S](https://store.mesanet.com/index.php?route=product/product&product_id=374) (or 7i76E)  
* [THCAD-10](https://store.mesanet.com/index.php?route=product/product&product_id=127) height sensing

### **Controller box**

* [Raycus RFL-C1500 User Guide](https://en.raycuslaser.com/upload/20220324/1futhmi6h1r9g1vrto.pdf)  
* [Maxphotonics MFSC 1000W-1500W Manual](https://pdf.directindustry.com/pdf/maxphotonics-co-ltd/mfp-series-q-switched-pulse-fiber-laser-user-s-guide/157735-629681.html): If cloudraw source uses the Maxphotonics "G3" architecture, this manual provides the specific 8-bit power bus logic (Pins 1-8).

### **Laser side signal condition on DB-25**

* Modulation (Pin 19): Use an RS-422 Differential Receiver to maintain a crisp 20kHz pulse and block EMI over the long cable run.  
* Power Supply: Tap Pin 17 (+5V) on the laser's DB25 to power your buffer circuit (verify voltage with a multimeter first).  
* Grounding: Use Pin 25 (GND) as your logic common; ensure the cable shield is grounded at the laser end only.  
* Safety Isolation: Use Optoisolators for low-speed logic (Enable, Ready, Error) to protect the Mesa board from high-voltage faults.  
* Hardware: House the circuit in a shielded aluminum box mounted directly to the laser using a DB25 Male-to-Male gender changer.  
* Cable Quality: Deploy a double-shielded industrial DB25 cable (foil \+ braid) to act as a barrier against servo motor noise.

### **DIN rail systems**

* 24V Field Power system, Mean Well [SDR-120-24](https://mou.sr/4vt2Dxf)  
* General purpose relay [38.52.7.024.0050](https://www.digikey.com/en/products/detail/finder-relays-inc/38.52.7.024.0050/10055815) and socket 93.02.7.024  
* [Narrow Slot Wire Duct](https://google.com/search?q=\(1%22+W+x+3%22+H\)+-+Black+Narrow+Slot+Wire+Duct+6.5%27&prds=headlineOfferDocid%3A3394051378468670811%2Cproductid%3A3394051378468670811%2Cpvo%3A38%2Cpvt%3Ahg&ibp=oshop&pvo=38&opi=103135050&gl=US&hl=en&noiga=1)  
* [Push-In Terminal Blocks](https://google.com/search?q=10pcs/set+PT+2.5+Push-In+Din+Rail+Mounted+Terminal+Blocks+Spring+Screwless+Feed,+Size:+24,+Gray&prds=headlineOfferDocid%3A9693193005356797468%2Cproductid%3A9693193005356797468%2Cpvo%3A38%2Cpvt%3Ahg&ibp=oshop&pvo=38&opi=103135050&gl=US&hl=en&noiga=1)  
* [Grounding Terminal Blocks](https://google.com/search?q=Siemens+Ground+Terminal+Block&prds=catalogid%3A8330128584833181567%2Cgpcid%3A10243653714409647064%2CheadlineOfferDocid%3A14112956594196320175%2Cmid%3A576462728235596048%2Cproductid%3A7214032751195772387%2Cpvo%3A38%2Cpvt%3Ahg&ibp=oshop&pvo=38&opi=103135050&gl=US&hl=en&noiga=1)

### **Height sensing:**

* Preamplifier (BCL-AMP), Converts capacitance to 0-10V for the THCAD.  
* Ceramic Ring, Isolates the nozzle to act as a sensor.  
* Shielded Coax Cable, Connects nozzle to Preamplifier.  
* Isolated 24V PSU, Eliminates signal noise from the 1.5kW source.

### **Chiller**

* The  [**S\&A CWFL-1500**](https://google.com/search?q=S%26A+CWFL-1500+Industrial+Water+Chiller+For+1500W+Fiber+Laser+Cutting+Machine&prds=headlineOfferDocid%3A17375003498786172168%2Cproductid%3A17375003498786172168%2Cpvo%3A38%2Cpvt%3Ahg&ibp=oshop&pvo=38&opi=103135050&gl=US&hl=en&noiga=1) dual circuit chiller

### **Gas control**

* ### [**https://alleriastore.com/products/auxiliary-gas-control-system**](https://alleriastore.com/products/auxiliary-gas-control-system)

* [Travis Mitchell](https://www.patreon.com/DIYfiberlaser) patreon site has a bill of materials

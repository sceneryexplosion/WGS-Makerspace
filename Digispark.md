# Installation av programvara
1. Installera arduino IDE version 1.6.5  https://www.arduino.cc/en/software/OldSoftwareReleases
2. Efter installationen starta programmet 
3. Gå till **File** (fil) --> **Preferences** (inställningar)
4. I rutan där det står “Additional Boards Manager URLs” kopiera och klistra in

   http://digistump.com/package_digistump_index.json

      ![](http://digistump.com/wiki/_media/digispark/tutorials/entry.jpg)
5. Klicka **OK**
6. Gå till **Tools** (Verktyg) --> **Board** --> **Boards Manager**
7. Ändra type från **All** till **Contributed**

8. Välj "Digistump AVR Boards" och klicka installera
   ![](http://digistump.com/wiki/_media/digispark/tutorials/digispark_install.gif)
9. En popup kommer att komma för att installera drivrutiner, godkänn dessa. En av drivrutinerna kan misslyckas vid installationen, strunta i detta, det kommer att fungera ändå. 
10. När installationen är klar gå till Board --> Digispark (Default - 16.5Mhz)
    ![](http://digistump.com/wiki/_media/digispark/tutorials/pickdigispark.gif)

# Skriv kod!

Kopiera alllt nedanför och klistra in i Arduino IDE.
```
// Allting i void setup funtionen körs en gång när digisparken strömsätts

void setup() {                
  // Definera benet som led lampan är kopplad på som en OUTPUT
  pinMode(0, OUTPUT); //LED på Model B
  pinMode(1, OUTPUT); //LED på Model A   
}

// Allting i loop funktionen körs om och om igen
void loop() {
  digitalWrite(0, HIGH);   // Tänd LED lampan 
  digitalWrite(1, HIGH);
  delay(1000);               // Vänta i 1000 millisekunder
  digitalWrite(0, LOW);    // Släck LED lampan
  digitalWrite(1, LOW); 
  delay(1000);               // Vänta i 1000 millisekunder
}
```

# Ladda upp
Tryck på **Upload** (ladda upp) **innan** du kopplar in digisparken i USB porten. Du har Ca 60 sekunder på dig att koppla in digisparken i USB-porten från att du tryckt på knappen.

# Referenser
Pin outs:

All pins can be used as Digital I/O
- Pin 0 → I2C SDA, PWM (LED on Model B)
- Pin 1 → PWM (LED on Model A)
- Pin 2 → I2C SCK, Analog In
- Pin 3 → Analog In (also used for USB+ when USB is in use)
- Pin 4 → PWM, Analog (also used for USB- when USB is in use)
- Pin 5 → Analog In


## Guiden som informationen här är hämtad ifrån
http://digistump.com/wiki/digispark/tutorials/connecting

## Bra sidor att hitta inspiration
1. https://github.com/CedArctic/DigiSpark-Scripts
2. http://digistump.com/wiki/digispark
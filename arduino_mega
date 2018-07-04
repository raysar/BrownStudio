//rgb
#include <FastLED.h>
#define DATA_PIN     46
#define NUM_LEDS    50
#define BRIGHTNESS  64
//#define LED_TYPE    UCS1903
#define LED_TYPE    WS2811
#define COLOR_ORDER GRB
CRGB leds[NUM_LEDS];
#define UPDATES_PER_SECOND 100

#include <DHT.h>
#include <DHT_U.h>

/* Inclut la librairie LiquidCrystal pour le LCD */
#include <LiquidCrystal.h>
#include "Menu.h" // Fichier d'entête avec les types pour le menu
 
/* Objet LCD sur les broches utilisées par la shield LCD DFrobots */
static LiquidCrystal lcd(8, 9, 4, 5, 6, 7);

// pour le capteur de température
//#define DHTTYPE DHT22   // DHT 22  (AM2302
//#define DHTPin 19
DHT dht2(47,DHT22);

//Adafruit_NeoPixel pixels = Adafruit_NeoPixel(15,16,NEO_GRB + NEO_KHZ400);


void doMainMenuAction(byte selectedMenuItem);
void doFreemanMenuAction(byte selectedMenuItem);
void doSubMainMenuAction(byte selectedMenuItem);
 
/* Menu principal */
static const char* MAIN_MENU_ITEMS[] = {
  "1 pleine lum",
  "2 douche",
  "3 plafond",
  "4 bandeau 50%",
  "5 bandeau 100%",
  "6 tamise",
  "7 temp/humid"
};
static const Menu_t MAIN_MENU = {
  "YO BROWN !",
  MAIN_MENU_ITEMS,
  7,
  &doMainMenuAction
};
 
/* Sous menu pour Dr Freeman */
static const char* FREEMAN_MENU_ITEMS[] = {
  "Gordon Freeman",
  "Morgan Freeman",
  "Martin Freeman"
};
static const Menu_t FREEMAN_MENU = {
  "Votre choix ?",
  FREEMAN_MENU_ITEMS,
  3,
  &doFreemanMenuAction
};
 
/** Setup */
void setup() {

  FastLED.addLeds<UCS1903, DATA_PIN, RGB>(leds, NUM_LEDS);
 
  /* Configuration du LCD */
  lcd.begin(16, 2);
  //Serial.begin(9600);
  //Serial.println("test1");
  pinMode(15, OUTPUT);
  pinMode(16, OUTPUT);
  pinMode(17, OUTPUT);
  pinMode(18, OUTPUT);
  pinMode(44, OUTPUT);
  pinMode(45, OUTPUT);
//  pinMode(46, OUTPUT);

  pinMode(22, OUTPUT);
  pinMode(24, OUTPUT);
  pinMode(26, OUTPUT);
  pinMode(28, OUTPUT);
  pinMode(30, OUTPUT);
  pinMode(32, OUTPUT);
  pinMode(34, OUTPUT);
  pinMode(36, OUTPUT);

  pinMode(23, OUTPUT);
  pinMode(25, OUTPUT);
  pinMode(27, OUTPUT);
  pinMode(29, OUTPUT);
  pinMode(31, OUTPUT);
  pinMode(33, OUTPUT);
  pinMode(35, OUTPUT);
  pinMode(37, OUTPUT);

  digitalWrite(22, HIGH);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, HIGH);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, HIGH);
  digitalWrite(36, HIGH);
  digitalWrite(23, HIGH);
  digitalWrite(25, HIGH);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, HIGH);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, HIGH);

//  digitalWrite(22, LOW);
//  delay(300);
//  digitalWrite(24, LOW);
//  digitalWrite(22, HIGH);
//  delay(300);
//  digitalWrite(26, LOW);
//  digitalWrite(24, HIGH);
//  delay(300);
//  digitalWrite(28, LOW);
//  digitalWrite(26, HIGH);
//  delay(300);
//  digitalWrite(30, LOW);
//  digitalWrite(28, HIGH);
//  delay(300);
//  digitalWrite(32, LOW);
//  digitalWrite(30, HIGH);
//  delay(300);
//  digitalWrite(34, LOW);
//  digitalWrite(32, HIGH);
//  delay(300);
//  digitalWrite(36, LOW);
//  digitalWrite(34, HIGH);
//  
//  delay(300);
//  digitalWrite(23, LOW);
//  digitalWrite(36, HIGH);
//  delay(300);
//  digitalWrite(25, LOW);
//  digitalWrite(23, HIGH);
//  delay(300);
//  digitalWrite(27, LOW);
//  digitalWrite(25, HIGH);
//  delay(300);
//  digitalWrite(29, LOW);
//  digitalWrite(27, HIGH);
//  delay(300);
//  digitalWrite(31, LOW);
//  digitalWrite(29, HIGH);
//  delay(300);
//  digitalWrite(33, LOW);
//  digitalWrite(31, HIGH);
//  delay(300);
//  digitalWrite(35, LOW);
//  digitalWrite(23, HIGH);
//  delay(300);
//  digitalWrite(37, LOW);
//  digitalWrite(35, HIGH);
//  delay(300);
//  digitalWrite(37, LOW);

  
  digitalWrite(22, LOW);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, LOW);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, LOW);
  digitalWrite(36, HIGH);
  digitalWrite(23, HIGH);
  digitalWrite(25, LOW);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, LOW);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, LOW);
  //delay(300);

  dht2.begin();

  for(int whiteLed = 0; whiteLed < NUM_LEDS; whiteLed = whiteLed + 1) {
      // Turn our current led on to white, then show the leds
      leds[whiteLed] = CRGB( 0, 0, 0);
      // Show the leds (only one of which is set to white, from above)
      FastLED.show();

      // Wait a little bit
      delay(10);

      // Turn our current led back to black for the next loop around
      leds[whiteLed] = CRGB( 0, 0, 0);
   }

//pwm bandeau 12v sur la sortie 3
//analogWrite(44, 0);
//delay(1000);
//analogWrite(44, 100);
//delay(1000);
//analogWrite(44, 0);
//delay(1000);
//analogWrite(44, 255);
//delay(1000);
//analogWrite(44, 30);
//delay(1000);

//for(int i=0; i <= 255; i++){
//analogWrite(44, i);
 
  //if (i == 254) {
  //  i = 0;
  //}
  // wait for 30 milliseconds to see the dimming effect
  //delay(20);
//}

//for(int i=0; i <= 255; i++){
//analogWrite(44, i);
 
  //if (i == 254) {
  //  i = 0;
  //}
  // wait for 30 milliseconds to see the dimming effect
//  delay(20);
//}
  analogWrite(44, 255);
  analogWrite(45, 255);
  //analogWrite(46, 255);

//  pixels.begin();
//  pixels.show();
//  for(int i = 0; i < 14; i++ ) { // On fait une boucle pour définir la couleur de chaque led
//        // setPixelColor(n° de led, Rouge, Vert, Bleu)
//        pixels.setPixelColor(i, pixels.Color(0,150,0));
//        
//      
//      pixels.show(); // on affiche
//      delay(1000);
//  }
}

 
/** Programme principal */
void loop() {

 
  /* Affiche le menu principal */
  displayMenu(MAIN_MENU);
 
  /* Démo pour montrer la sortie du menu */
  lcd.clear();
  lcd.print(F("Menu ferme"));
  delay(1000);
}
 
/** Fonction retournant le bouton appuyé (s’il y en a un). */
Button_t readPushButton(void) {
 
  /* Lecture de l'entrée A0 */
  unsigned int val = analogRead(A0);
 
  /* Test suivant les fourchettes de valeurs */
  if (val > 1000) return BP_NONE;
  if (val < 50) return BP_RIGTH;  
  if (val < 195) return BP_UP; 
  if (val < 380) return BP_DOWN; 
  if (val < 555) return BP_LEFT; 
  if (val < 790) return BP_SELECT;
 
  /* Par défaut aucun bouton n'est appuyé */
  return BP_NONE;
}
 
/** Affiche le menu passé en argument */
void displayMenu(const Menu_t &menu) {
 
  /* Variable pour le menu */
  byte selectedMenuItem = 0;   // Choix selectionné
  byte shouldExitMenu = false; // Devient true quand l'utilisateur veut quitter le menu
  Button_t buttonPressed;      // Contient le bouton appuyé
 
  /* Tant que l'utilisateur ne veut pas quitter pas le menu */
  while(!shouldExitMenu) {
 
    /* Affiche le menu */
    lcd.clear();
    lcd.print(menu.prompt);
    lcd.setCursor(0, 1);
    lcd.print(menu.items[selectedMenuItem]);
 
    /* Attend le relâchement du bouton */
    while(readPushButton() != BP_NONE);
 
    /* Attend l'appui sur un bouton */
    while((buttonPressed = readPushButton()) == BP_NONE);
 
    /* Anti rebond pour le bouton */
    delay(30);
 
    /* Attend le relâchement du bouton */
    while(readPushButton() != BP_NONE);
 
    /* Gére l'appui sur le bouton */
    switch(buttonPressed) {
    case BP_UP: // Bouton haut = choix précédent
 
      /* Si il existe un choix précédent */
      if(selectedMenuItem > 0) {
 
        /* Passe au choix précédent */
        selectedMenuItem--;
      }
      break;
 
    case BP_DOWN: // Bouton bas = choix suivant
 
      /* Si il existe un choix suivant */
      if(selectedMenuItem < (menu.nbItems - 1)) {
 
        /* Passe au choix suivant */
        selectedMenuItem++;
      }
      break;
 
    case BP_LEFT: // Bouton gauche = sorti du menu
      shouldExitMenu = true;
      break;
 
    case BP_SELECT: //
    case BP_RIGTH:  // Bouton droit ou SELECT = validation du choix
      menu.callbackFnct(selectedMenuItem);
      break;
    }
  }
}
 
/** Affiche le choix de l'utilisateur */
void doMainMenuAction(byte selectedMenuItem) {
  
  /* Gère le choix de l'utilisateur */
  switch(selectedMenuItem) {
  case 0:
    // allumé Code pour le choix 1
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix1");
  digitalWrite(22, LOW);
  digitalWrite(24, LOW);
  digitalWrite(26, LOW);
  digitalWrite(28, LOW);
  digitalWrite(30, LOW);
  digitalWrite(32, LOW);
  digitalWrite(34, LOW);
  digitalWrite(36, LOW);
  digitalWrite(23, LOW);
  digitalWrite(25, LOW);
  digitalWrite(27, LOW);
  digitalWrite(29, LOW);
  digitalWrite(31, LOW);
  digitalWrite(33, LOW);
  digitalWrite(35, LOW);
  digitalWrite(37, LOW);
  analogWrite(44, 0);
  analogWrite(45, 0);
  analogWrite(46, 0);
    break;
 
  case 1:
    // éteint Code pour le choix 2
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix2");
  digitalWrite(22, HIGH);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, HIGH);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, HIGH);
  digitalWrite(36, HIGH);
  digitalWrite(23, LOW);
  digitalWrite(25, LOW);
  digitalWrite(27, LOW);
  digitalWrite(29, LOW);
  digitalWrite(31, LOW);
  digitalWrite(33, LOW);
  digitalWrite(35, LOW);
  digitalWrite(37, LOW);
  analogWrite(44, 0);
  analogWrite(45, 0);
  analogWrite(46, 0);
    break;
 
  case 2:
    // allumé Code pour le choix 1
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix1");
  digitalWrite(22, LOW);
  digitalWrite(24, LOW);
  digitalWrite(26, LOW);
  digitalWrite(28, LOW);
  digitalWrite(30, LOW);
  digitalWrite(32, LOW);
  digitalWrite(34, LOW);
  digitalWrite(36, LOW);
  digitalWrite(23, HIGH);
  digitalWrite(25, HIGH);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, HIGH);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, HIGH);
  analogWrite(44, 0);
  analogWrite(45, 0);
  analogWrite(46, 0);
    break;

  case 3:
    // allumé Code pour le choix 1
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix1");
  digitalWrite(22, HIGH);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, HIGH);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, HIGH);
  digitalWrite(36, HIGH);
  digitalWrite(23, HIGH);
  digitalWrite(25, HIGH);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, HIGH);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, HIGH);
  analogWrite(44, 140);
  analogWrite(45, 140);
  analogWrite(46, 140);
    break;

      case 4:
    // allumé Code pour le choix 1
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix1");
  digitalWrite(22, HIGH);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, HIGH);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, HIGH);
  digitalWrite(36, HIGH);
  digitalWrite(23, HIGH);
  digitalWrite(25, HIGH);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, HIGH);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, HIGH);
  analogWrite(44, 255);
  analogWrite(45, 255);
  analogWrite(46, 255);
  //for(int boucle=0 ; boucle<20 ; boucle++){
for(int whiteLed = 0; whiteLed < NUM_LEDS; whiteLed = whiteLed + 1) {
      // Turn our current led on to white, then show the leds
      leds[whiteLed] = CRGB( 20, 255, 0);
      // Show the leds (only one of which is set to white, from above)
      FastLED.show();

      // Wait a little bit
      delay(100);

      // Turn our current led back to black for the next loop around
      leds[whiteLed] = CRGB( 20, 255, 0);
   }
//}
    break;

  case 5:
    // tamisé
    //Serial.println(selectedMenuItem);
    //Serial.println("test choix1");
  digitalWrite(22, LOW);
  digitalWrite(24, HIGH);
  digitalWrite(26, HIGH);
  digitalWrite(28, LOW);
  digitalWrite(30, HIGH);
  digitalWrite(32, HIGH);
  digitalWrite(34, LOW);
  digitalWrite(36, HIGH);
  digitalWrite(23, HIGH);
  digitalWrite(25, LOW);
  digitalWrite(27, HIGH);
  digitalWrite(29, HIGH);
  digitalWrite(31, LOW);
  digitalWrite(33, HIGH);
  digitalWrite(35, HIGH);
  digitalWrite(37, LOW);
  analogWrite(44, 50);
  analogWrite(45, 50);
  analogWrite(46, 50);
    break;

 case 6:
  //température
  // Sensor readings may also be up to 2 seconds 'old' (its a very slow sensor)
  float h = dht2.readHumidity();
  // Read temperature as Celsius (the default)
  float t = dht2.readTemperature();
  lcd.setCursor(0,0); // Sets the location at which subsequent text written to the LCD will be displayed
  lcd.print("Temp.: "); // Prints string "Temp." on the LCD
  lcd.print(t); // Prints the temperature value from the sensor
  lcd.print(" C");
  lcd.setCursor(0,1);
  lcd.print("Humi.: ");
  lcd.print(h);
  lcd.print(" %");
  delay(3000);
  break;
  }
  /* Affiche le choix de l'utilisateur */
    displayChoice(selectedMenuItem, MAIN_MENU_ITEMS);
 
}
 
/** Affiche le choix de l'utilisateur */
void doFreemanMenuAction(byte selectedMenuItem) {
 
  /* Affiche le choix de l'utilisateur */
  displayChoice(selectedMenuItem, FREEMAN_MENU_ITEMS);
}
 
/** Affiche le choix de l'utilisateur */
void displayChoice(byte selectedMenuItem, const char** items) {
 
  /* Affiche le choix de l'utilisateur */
  lcd.clear();
  lcd.print(F("vs avez choisi:"));
  lcd.setCursor(0, 1);
  lcd.print(items[selectedMenuItem]);
 
  /* Attend l'appui sur le bouton gauche ou SELECT */
  byte buttonPressed;
  do {
    buttonPressed = readPushButton();
  } 
  while(buttonPressed != BP_LEFT && buttonPressed != BP_SELECT);
}

#include <SoftwareSerial.h>
#include <DFRobotDFPlayerMini.h>

SoftwareSerial mySoftwareSerial(10, 11); // RX, TX
DFRobotDFPlayerMini myDFPlayer;
void printDetail(uint8_t type, int value);
const int PEEL1 = 2;
const int PEEL2 = 3;
const int PEEL3 = 4;
const int PEEL4 = 5;
int counter = 0;

boolean isPlaying = false;
boolean played1 = false;
boolean played2 = false;
boolean played3 = false;
boolean played4 = false;

void setup() {
  mySoftwareSerial.begin(9600);
  Serial.begin(115200);

  Serial.println();
  Serial.println(F("DFRobot DFPlayer Mini Demo"));
  Serial.println(F("Initializing DFPlayer ... (May take 3~5 seconds)"));

  if (!myDFPlayer.begin(mySoftwareSerial)) {  //Use softwareSerial to communicate with mp3.
    Serial.println(F("Unable to begin:"));
    Serial.println(F("1.Please recheck the connection!"));
    Serial.println(F("2.Please insert the SD card!"));
    while (true);
  }
  Serial.println(F("DFPlayer Mini online."));

  pinMode(PEEL1, INPUT);
  pinMode(PEEL2, INPUT);
  pinMode(PEEL3, INPUT);
  pinMode(PEEL4, INPUT);
}

void loop() {

  if (digitalRead(PEEL1) == LOW && played1 == false) {
    //      Serial.println("I am on");
    myDFPlayer.volume(30);
    myDFPlayer.play(counter);
    delay(1000);
    counter = counter + 1;
    Serial.println(counter);
    if (counter == 41) {
      counter = 0;
    }
    played1 = true;
  }

  if (digitalRead(PEEL1) == HIGH) {
    played1 = false;
  }


  if (digitalRead(PEEL2) == LOW && played2 == false) {
    //      Serial.println("I am on");
    myDFPlayer.volume(30);
    myDFPlayer.play(counter);
    delay(1000);
    counter = counter + 1;
    Serial.println(counter);
    if (counter == 41) {
      counter = 0;
    }
    played2 = true;
  }

  if (digitalRead(PEEL2) == HIGH) {
    played2 = false;
  }

  if (digitalRead(PEEL3) == LOW && played3 == false) {
    //      Serial.println("I am on");
    myDFPlayer.volume(30);
    myDFPlayer.play(counter);
    delay(1000);
    counter = counter + 1;
    Serial.println(counter);
    if (counter == 41) {
      counter = 0;
    }
    played3 = true;
  }

  if (digitalRead(PEEL3) == HIGH) {
    played3 = false;
  }

  if (digitalRead(PEEL4) == LOW && played4 == false) {
//    Serial.println("I am on");
    myDFPlayer.volume(30);
    myDFPlayer.play(counter);
    delay(1000);
    counter = counter + 1;
    Serial.println(counter);
    if (counter == 41) {
      counter = 0;
    }
    played4 = true;
  }

  if (digitalRead(PEEL4) == HIGH) {
    played4 = false;
  }

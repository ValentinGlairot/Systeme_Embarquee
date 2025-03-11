#include <limits.h>

const long Vitesse_de_la_lumiere = 299792458;

long Distance = INT_MIN;
bool Success;


bool Multiplier(long &parametre) {
    parametre *= Vitesse_de_la_lumiere;
    if (parametre < 1) {
        return false;
    }
    return true;
}

void setup() {
    Serial.begin(9600);
    pinMode(13, OUTPUT);
    Success = true;
    while (Success) {
        Success = Multiplier(Distance);
        Serial.println(Distance);
    }
  
    digitalWrite(13, HIGH);
}

void loop() {
  
}

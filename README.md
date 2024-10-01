The development of LPG (Liquefied Petroleum Gas) leakage detection alert and auto exhaust is an 
important safety measure in today's world. LPG is a highly flammable and explosive gas that is used 
in many households and industries for cooking and heating purposes. However, LPG leakage can pose 
a serious threat to human life and property, as it can cause fires, explosions, and even death.  
  
To prevent such accidents, LPG leakage detection alert and auto exhaust systems have been developed. 
These systems use sensors to detect any leakage of LPG and automatically shut off the gas supply, 
preventing any further leakage. In addition, an alarm is sounded to alert the occupants of the building 
about the danger.  
  
The auto exhaust system is designed to expel the leaked gas from the building to prevent it from 
accumulating and causing an explosion. The system includes exhaust fans that are activated 
automatically when the sensors detect a leakage of LPG. The fans suck the gas out of the building and 
expel it outside, reducing the risk of an explosion.  
  
The development of LPG leakage detection alert and auto exhaust systems has been a significant step 
in ensuring the safety of people and property. These systems have been widely adopted in households 
and industries, reducing the risk of LPG-related accidents. 

PROBLEM DEFINITION:   
The problem that the development of LPG leakage detection alert and auto exhaust systems  
aims to solve is the safety risks posed by LPG leakage in industries and households. LPG is a  
highly flammable and explosive gas that can cause fires, explosions, and even death if not  
handled properly.  
The traditional methods of detecting LPG leakage, such as LPG gas sensors, were not effective  
in preventing accidents. Therefore, there was a need for a more efficient and effective method  
of detecting LPG leakage and preventing accidents.  
The development of LPG leakage detection alert and auto exhaust systems addresses this  
problem by using sensors that can detect even minor leaks of LPG and automatically shut off  
the gas supply. In addition, the alarm sounds to alert the occupants of the building about the  
danger, while the auto exhaust system expels the leaked gas from the building, reducing the  
risk of an explosion.  
This problem is particularly relevant in industries and households that use LPG as a fuel, as the  
risks of LPG leakage are higher in such environments. Therefore, the development of LPG  
leakage detection alert and auto exhaust systems is crucial in ensuring the safety of people and  
property in such settings.


CODE IN JAVA:
import java.util.Random;

class LPGLeakageSystem {
    private static final double THRESHOLD = 5.0;  // Example threshold value
    private boolean alertOn = false;
    private boolean exhaustOn = false;

    // Simulates gas level detection from a sensor
    public double detectGasLevel() {
        Random random = new Random();
        return 10 * random.nextDouble();  // Random gas level between 0 and 10
    }

    // Checks if gas level exceeds the threshold
    public void checkForLeakage() {
        double gasLevel = detectGasLevel();
        System.out.println("Gas Level Detected: " + gasLevel + " ppm");

        if (gasLevel > THRESHOLD) {
            activateAlert();
            turnOnExhaust();
        } else {
            deactivateAlert();
            turnOffExhaust();
        }
    }

    // Activates alert system
    private void activateAlert() {
        if (!alertOn) {
            System.out.println("ALERT! Gas leakage detected.");
            alertOn = true;
        }
    }

    // Deactivates alert system
    private void deactivateAlert() {
        if (alertOn) {
            System.out.println("Safe! No leakage detected.");
            alertOn = false;
        }
    }

    // Turns on the exhaust system
    private void turnOnExhaust() {
        if (!exhaustOn) {
            System.out.println("Exhaust system ON. Ventilating area...");
            exhaustOn = true;
        }
    }

    // Turns off the exhaust system
    private void turnOffExhaust() {
        if (exhaustOn) {
            System.out.println("Exhaust system OFF. Area is safe.");
            exhaustOn = false;
        }
    }

    public static void main(String[] args) {
        LPGLeakageSystem system = new LPGLeakageSystem();
        while (true) {
            system.checkForLeakage();
            try {
                Thread.sleep(5000);  // Wait 5 seconds before next detection
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

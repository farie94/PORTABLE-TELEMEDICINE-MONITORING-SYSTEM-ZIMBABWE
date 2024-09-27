# PORTABLE-TELEMEDICINE-MONITORING-SYSTEM-ZIMBABWE

Doctor logs in , Patient logs in by filling his issues.
Both go in to video conference call and discuss issues.
Doctor fills advice.
Patient can print advice after the call.
Doctor and patients can also send chat messages to each other.
Patients can also share documents with doctor.
Features :-

Application supports Multi doctor and Multihospital.

Medication can be filled by Doc

Patient can input problems

Chat message support between doctors and patients.

Patients can share document with doctors while conferencing.

Tracks time spent per call between doctor and patient.


// Define a class for Telemedicine Monitoring System
class TelemedicineMonitoringSystem {
private:
    std::string patientName;
    std::string country;
    int heartRate;
    int systolicBP;
    int diastolicBP;
    float temperature;

public:
    TelemedicineMonitoringSystem(std::string name, std::string country) {
        patientName = name;
        this->country = country;
        heartRate = 0;
        systolicBP = 0;
        diastolicBP = 0;
        temperature = 0.0f;
    }

    void updateVitalSigns(int hr, int sysBP, int diaBP, float temp) {
        heartRate = hr;
        systolicBP = sysBP;
        diastolicBP = diaBP;
        temperature = temp;
    }

    void displayVitalSigns() {
        std::cout << "Patient: " << patientFarai << " from " << country << std::endl;
        std::cout << "Heart Rate: " << heartRate << std::endl;
        std::cout << "Blood Pressure: " << systolicBP << "/" << diastolicBP << std::endl;
        std::cout << "Temperature: " << temperature << " Celsius" << std::endl;
    }
};

int main() {
    TelemedicineMonitoringSystem patientMonitor("Farai Nyasango", "Zimbabwe");

    // Update and display vital signs
    patientMonitor.updateVitalSigns(75, 120, 80, 37.2);
    patientMonitor.displayVitalSigns();

    return 0;
}

# PORTABLE-TELEMEDICINE-MONITORING-SYSTEM-ZIMBABWE
PTMSZ

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
        std::cout << "Patient: " << patientName << " from " << country << std::endl;
        std::cout << "Heart Rate: " << heartRate << std::endl;
        std::cout << "Blood Pressure: " << systolicBP << "/" << diastolicBP << std::endl;
        std::cout << "Temperature: " << temperature << " Celsius" << std::endl;
    }
};

int main() {
    TelemedicineMonitoringSystem patientMonitor("John Doe", "Zimbabwe");

    // Update and display vital signs
    patientMonitor.updateVitalSigns(75, 120, 80, 37.2);
    patientMonitor.displayVitalSigns();

    return 0;
}

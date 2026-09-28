# Distribution-line-monitoring
# Distribution Line Monitoring System

MIN_VOLTAGE = 200
MAX_VOLTAGE = 250
MAX_CURRENT = 100
MAX_TEMPERATURE = 75

print("==============================")
print(" DISTRIBUTION LINE MONITORING")
print("==============================")

voltage = float(input("Enter line voltage (V): "))
current = float(input("Enter line current (A): "))
temperature = float(input("Enter line temperature (°C): "))

fault = False

print("\n--- Line Monitoring Data ---")
print("Voltage    :", voltage, "V")
print("Current    :", current, "A")
print("Temperature:", temperature, "°C")

# Voltage monitoring
if voltage < MIN_VOLTAGE:
    print("⚠️ Under-voltage detected")
    fault = True

elif voltage > MAX_VOLTAGE:
    print("⚠️ Over-voltage detected")
    fault = True

# Current monitoring
if current > MAX_CURRENT:
    print("⚠️ Overcurrent detected")
    fault = True

# Temperature monitoring
if temperature > MAX_TEMPERATURE:
    print("⚠️ High line temperature detected")
    fault = True

# Final status
if fault:
    print("\n🔴 DISTRIBUTION LINE ALERT")
    print("⚠️ Abnormal condition detected")
    print("🚨 Maintenance required")

else:
    print("\n🟢 DISTRIBUTION LINE STATUS: NORMAL")
    print("✅ Line is operating safely")
    

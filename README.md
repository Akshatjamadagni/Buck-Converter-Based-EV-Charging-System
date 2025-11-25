# Buck Converter Based EV Charging System

## Project Overview
This project presents the design and simulation of a DC-DC Buck Converter for electric vehicle (EV) and e-bike battery charging applications. The converter efficiently steps down 325V DC input to 48V DC output suitable for battery charging.

## Team Members
- **Akshat Kumar** (12240080)
- **Ayush Kumar Mishra** (12240340)

## Project Specifications

| Parameter | Value |
|-----------|-------|
| Input Voltage | 325V DC |
| Output Voltage | 48V DC |
| Output Current | 3A |
| Output Power | 144W |
| Switching Frequency | 50 kHz |
| Duty Cycle | 14.8% |

## Key Components
- **MOSFET**: STW11NM80 (Main switching element)
- **Diode**: MUR460 (Freewheeling diode)
- **Inductor**: 1 mH (Energy storage)
- **Capacitor**: 470 µF (Output filtering)
- **Load Resistor**: 16 Ω

## Working Principle
The buck converter operates in two phases:
1. **MOSFET ON**: Energy is stored in the inductor from the input source
2. **MOSFET OFF**: Stored energy is released to the load through the freewheeling diode

The output voltage is controlled by adjusting the PWM duty cycle, maintaining stable 48V output for battery charging.

## Simulation Details
- **Software**: LTspice
- **PWM Configuration**: `PULSE(0 10 0 10n 10n 2.96u 20u)`
- **Transient Analysis**: `.tran 0 10m 5m`
- **Startup Time**: ~5 ms to reach steady-state

## Key Results
✅ Successful voltage conversion from 325V to 48-55V  
✅ Average output current of 3A achieved  
✅ Stable operation at 50 kHz switching frequency  
✅ Continuous Conduction Mode (CCM) operation  
✅ Estimated efficiency: >90%  
✅ Acceptable voltage and current ripple characteristics  

## Applications
- Small electric vehicle charging stations
- E-bike battery chargers
- Industrial DC power supplies
- UPS (Uninterruptible Power Supply) systems
- Solar battery charging systems

## Advantages
- High power efficiency (>90%)
- Simple circuit topology with minimal components
- Cost-effective implementation
- Smooth DC output suitable for battery charging
- Easy PWM control
- Lower switching losses

## Project Files
```
├── Presentation.pptx          # Project presentation slides
├── circuit_schematic.png     # LTspice circuit diagram
├── simulation_results/       # Voltage and current waveforms
├── buck convertor.asc         
└── README.md                # This file
```

## How to Run the Simulation
1. Open LTspice
2. Create new schematic with components as specified
3. Configure PWM source: `PULSE(0 10 0 10n 10n 2.96u 20u)`
4. Add transient analysis directive: `.tran 0 10m 5m`
5. Run simulation and observe output voltage and inductor current

## Future Enhancements
- Implement closed-loop feedback control for better voltage regulation
- Add synchronous rectification to improve efficiency
- Include overcurrent and overvoltage protection
- Design input/output EMI filters
- Develop hardware prototype for experimental validation
- Integrate smart charging algorithms with microcontroller

## Conclusion
This project successfully demonstrates the design and simulation of a buck converter suitable for low-to-medium power EV charging applications. The simulation results validate the theoretical design and confirm stable, efficient operation with acceptable ripple characteristics.

## Course
**Circuit & Systems Project**  
LTspice Simulation

---

*For detailed analysis, design calculations, and comprehensive results, please refer to the complete technical report.*

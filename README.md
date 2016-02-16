# Flight


import math
h=float(input("Enter height (km): "))

if h<11: #Troposphere 0-11

        T = float(288.15 - 6.5*h)
        p = float(101325.0 * (288.15 / (288.15 - 6.5*h)) **(34.1632 /-6.5))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)

elif h>=11: #Stratosphere 11-20

        T = float(216.65)
        p =float(22632.06 *math.exp(-34.1632 *(h-11) / 216.65))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)

elif h>=20: #Stratosphere 20-32

        T = float(196.65 + h)
        p = float(5474.889 * (216.65 / (216.65 + (h - 20))) (34.1632))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)
        
elif h>=32: #Stratosphere 32-47

        T = float(139.05 + 2.8 * h)
        p = float(868.0187 * (228.65 / (228.65 + 2.8 * (h - 32)))(34.1632 / 2.8))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)

elif h>=47: #Mesosphere 47-51

        T = float(270.65)
        p = float(110.9063 * math.exp(-34.1632 * (h - 47) / 270.65))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)

elif h>=51: #Mesosphere 51-71

        T = float(413.45 - 2.8 * h)
        p = float(66.93887 * (270.65 / (270.65 - 2.8 * (h - 51))) (34.1632 / -2.8))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)

elif h>=71: #Mesosphere 71-85

        T = float(356.65 - 2.0 * h)
        p = float(3.956420 * (214.65 / (214.65 - 2 * (h - 71))) (34.1632 / -2))
        print("Height (km):",h,", Temp (K):",T,", Pressure (Pa):",p)


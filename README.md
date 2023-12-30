# odometer




def func():
    start_odometer = float(input("Enter the starting odometer >>"))
    odometer = input("Enter the odometer reading for this leg >>")
    #leg_odometer = odometer - start_odometer
    count = 0
    trip_fuel_eff = 0
    while odometer:
        fuel_cons = float(input("Enter the fuel consumption for this leg >>"))
        odometer -= start_odometer
        fuel_eff = odometer/fuel_cons
        print("Fuel efficiency for this leg is", fuel_eff)
        start_odometer += odometer
        print("Start odometer is ", start_odometer)
        odometer = float(input("Enter the odometer reading for this leg >>"))
        #leg_odometer = odometer - start_odometer
        trip_fuel_eff += fuel_eff
        count += 1
    if count > 0:
        print("Fuel efficiency of the trip is", trip_fuel_eff / count)
    else:
        print("Fuel efficiency of the trip is unknown")

func()

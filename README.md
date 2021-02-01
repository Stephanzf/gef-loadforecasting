# gef-loadforecasting
This is a competition of the past (2012): https://www.kaggle.com/c/global-energy-forecasting-competition-2012-load-forecasting
Also ref: https://github.com/jingweikang/GlobalEnergyForecasting2012

# Research on
## How does zone load change or doesn't change with temperature?
for j in range(11):
    x = temp_stns_h1[:,j]
    for i in range(20):
        plt.scatter(x,load_zones_h1[:,i])
        plt.xlabel("Station "+ str(j+1) + " Temperature(F)")
        plt.ylabel("Zone " + str(i+1) +" Load(kW)")
        t = "zone" + str(i+1)+ "T"+str(j+1)+".png"
        plt.savefig(t, dpi=100)
        plt.show()
 
 As we can't associate temperature measurement points with load zones, we will plot all possible combinations: load vs temp. Please see the /images for all plots.
 
  https://github.com/Stephanzf/gef-loadforecasting/blob/master/zone9_load_vs_temperature.png  
  
  It looks like that only zone 9 load doesn't change with temperature. All the rest zone loads change with temperature. 
  
  ## How does zone load change with time, day, week, month, or season? 
  This is a major concern in power system daily operations: to forecast day ahead based on found patterns in the system.
  
  

# Entites that can be set up in the configuration.yaml file
## input_boolean
These are used for switches as either on or off
```
input_boolean:
  Switch1:          #name of entity
    initial: off    #intial state when first turned on
  Switch2:          #name of entity
    initial: off    #intial state when first turned on
```
when you call and input_boolean it will be address i.e. `input_boolean.Switch1`
In appdeamon this can be called by `self.get_state("input_boolean.pbr_auto_man")` This will return a 'on' or 'off'
to convert to a int/byte you can do the following:
```
Switch1_State = self.get_state("input_boolean.Switch1")
if Switch1_State == 'off':
    Switch1_State=0
else:
    Switch1_State=1
```
In appdaemon you can also set the sate by `self.turn_on('input_boolean.Switch1')` which you would call if a condition was met

## input_number

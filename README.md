# Wemo Emulation Server
Emulates multiple devices on RaspberryPi (or anything running Node.Js) as Wemo Switches and executes commands described in the configuration

```
// Example Configuration
{
	"Terminal A":{ 
		"oncommand": "/bin/chvt 1" 
	},

	"Display": { 
		"oncommand"  : "/opt/vc/bin/tvservice -p",
		"offcommand" : "/opt/vc/bin/tvservice -o"
	}

}
```

##Installation
```
// Install Globally
sudo npm install node-raspberry -g
```

##Execution
```
// Place devices.json in the execution path
node app
```
or

```
// Provide file path as
node app ./examples/devices.json
node app /etc/wemo/devices.json
```


##Usage
Use the alexa app on your cell phone/tablet to search for devices

```
Alexa turn on 'Display'
```
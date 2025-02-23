# Govee-Water-Leak-Home-Assistant-Autodiscovery
Autodiscovery script for Home Assistant. Creates devices in HA for Govee Water Leak Sensors (model H5054) that are populated in MQTT by RTL_433.

## Instructions: 
  1. Copy the yaml file contents into your configuration.yaml, or if you use packages save the entire YAML file
     in your packages folder.
  2. Edit line 19 with your MQTT discovery prefix and line 21 with the Govee main topic
  3. Create a list of leak sensor devices starting on line 27
  4. In Home Assistant, go to developer tools > YAML and click SCRIPTS to reload them.
  5. In Home Assistant, go to 'automations' > 'scripts' and run 'Govee Leak Device Autodiscovery Creator'.
     
#### (Optional:)
  6. Modify, add, or remove any sensor starting on line 56. All entries under the "config:" key are documented here:
     https://www.home-assistant.io/integrations/sensor.mqtt/#configuration-variables
     In order to pass a template, the brackets must be commented out. Use the following example as a reference:
     `value_template: "{{ '{{' }} value | float(0) * 1.234 {{ '}}' }}"`

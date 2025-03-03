
*To contribute to this page, edit the following
[file](https://github.com/Koenkk/zigbee2mqtt.io/blob/master/docgen/device_page_notes.js)*

# Device

| Model | AIRAM-CTR.U  |
| Vendor  | Airam  |
| Description | CTR.U remote (can only be used to control the Airam 4713407 bulb) |
| Supports | on/off |
| Picture | ![../images/devices/AIRAM-CTR.U.jpg](../images/devices/AIRAM-CTR.U.jpg) |

## Notes

None

## Manual Home Assistant configuration
Although Home Assistant integration through [MQTT discovery](../integration/home_assistant) is preferred,
manual integration is possbile with the following configuration:


### AIRAM-CTR.U
{% raw %}
```yaml
sensor:
  - platform: "mqtt"
    state_topic: "zigbee2mqtt/<FRIENDLY_NAME>"
    availability_topic: "zigbee2mqtt/bridge/state"
    unit_of_measurement: "-"
    value_template: "{{ value_json.linkquality }}"
```
{% endraw %}



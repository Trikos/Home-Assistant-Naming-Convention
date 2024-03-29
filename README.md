# Home Assistant Naming Convention
A repository dedicated to best practices for naming devices, sensors, and entities in Home Assistant setups. Includes a comprehensive guide to maintaining an organized and manageable smart home ecosystem.

## Table of Contents
1. [Naming convention](#comprehensive-naming-convention-for-home-assistant)
2. [Examples of entity_id](#examples-of-entity_id)
3. [Special Consideratons](#special-considerations-for-device-control-location-vs-function)
4. [Additional Notes](#additional-notes)

---

## Comprehensive Naming Convention for Home Assistant

To ensure consistency and ease of use within the Home Assistant environment, we use the following convention for naming `entity_id` for devices:

### General Structure:
```
<domain>.<location_code>_<device_type>_<function>_<identifier>
```

### Personal Devices:
```
<domain>.<user_code>_<device_type>_<identifier>
```

### Network Entities:
```
<domain>.<device_type>_<function>_<identifier>
```

_Where:_

- **`<location_code>`**: Indicates the specific location where the device is installed or controlled.
- **`<device_type>`**: Represents the type of device.
- **`<function>`**: Detail that provides additional information about the specific function of the device.
- **`<identifier>`**: Number or short name that distinguishes similar devices.
- **`<user_code>`**: Initials or nickname of the device owner.
- **`<domain>`**: The term 'domain' refers to a category or class of entities within the Home Assistant
system. For example, 'light' is a domain that represents all lighting entities, while 'sensor' 
represents sensor-type entities. Domains are used to organize and categorize entities based on 
their functions. In general, domains are not user-defined but are predefined in Home Assistant to 
represent various types of devices or functions. Here is a list of some _domains_: `person`, `sensor`, `media_player`, `light`, `switch`, `binary_sensor`, `device_tracker`

---

### Examples of `entity_id`

#### General Structure:
- `light.kitchen_light_1` - The first light bulb installed in the kitchen.
- `sensor.bedroom1_thermostat_temperature` - Thermostat for temperature in the first bedroom.
- `switch.garage_switch_door` - Switch for the garage door.
- `binary_sensor.livingroom_sensor_motion` - Motion sensor in the living room.
- `switch.bathroom_plug_heater` - Controlled outlet for the heater in the bathroom.

#### Personal Devices:

- `device_tracker.john_main_phone` - John Doe's main mobile phone.
- `device_tracker.maria_apple_watch` - Maria Bianchi's Apple Watch.

#### Network Entities:

- `switch.fritzbox_connection_status` - Internet connection status of the Fritz!Box modem/router.
- `switch.fritzbox_device_john_phone` - Fritz!Box network device associated with John Doe's mobile phone.
- `switch.fritzbox_john_phone_internet_access` - Internet connection access for John Doe's mobile phone.

---

#### Entity ID naming convention:
Entity IDs in Home Assistant have specific naming conventions that should be followed to ensure consistency and compatibility. Here are some important guidelines:

- *<b>Lowercase Characters Only:</b>* Entity IDs must consist of lowercase characters and can include underscores. Using uppercase characters or other special characters in entity IDs is not allowed.
  - Example of <b>valid</b> entity ID: `sensor.temperature_sensor`
  - Example of <b>invalid</b> entity ID: `sensor.TemperatureSensor`

- *<b>Use Descriptive Names:</b>* While keeping entity IDs short is helpful, it's also essential to make them descriptive. Choose names that clearly represent the entity's function or purpose.
  - Example of a <b>good</b> entity ID: `sensor.living_room_temperature`
  - Example of a <b>less descriptive</b> entity ID: `sensor.temp1`

- *<b>Avoid Special Characters:</b>* Do not use special characters, spaces, or punctuation marks in entity IDs. Stick to alphanumeric characters and underscores.
  - Example of <b>valid</b> entity ID: `sensor.office_thermostat`
  - Example of <b>invalid</b> entity ID: `sensor/kitchen@temperature`

--- 
### Special Considerations for Device Control Location vs. Function

In some cases, a device such as a switch may be physically located in one room but is used to control a device in another location. When naming these entities, you have two approaches:

1. **Based on the Physical Location of the Switch (I personally use this)**:
   - `switch.garage_garden_spotlights`:
     This naming emphasizes the physical location where the switch is positioned (the garage) and what it controls (the garden spotlights).
   

2. **Based on the Function of the Switch**:
   - `light.garden_garden_spotlights`:
     This naming indicates the function of the switch (controls spotlights) and the area it actually illuminates (garden), despite the physical location being in the garage. Using `light` instead of `switch` implies the specific use of turning on and off lights, which can be more intuitive if the switch is mainly used for this purpose.

---

### Additional Notes:

- It is important to document each newly added device according to this convention to maintain traceability and consistency.
- When applicable, use the location code where the device is located followed by the function it controls if it manages elements in another location (e.g., `switch.garage_switch_garden_lights` for a switch in the garage that turns on garden lights).
- Use intuitive names and identifiers to simplify understanding and use of `entity_id`.

Use this documentation as a reference for adding new devices to your Home Assistant system, modifying the nomenclature as necessary to adapt to new situations or devices. Maintain an accessible and updated registry to facilitate the scalability and maintenance of your home automation ecosystem.

---

Crafted by,

Your A.I. Home Assistant Guide Curator chatGPT (gpt-4-1106-preview)

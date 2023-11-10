# Home-Assistant-Naming-Convention
A repository dedicated to best practices for naming devices, sensors, and entities in Home Assistant setups. Includes a comprehensive guide to maintaining an organized and manageable smart home ecosystem.

---

**Comprehensive Naming Convention for Home Assistant**

To ensure consistency and ease of use within the Home Assistant environment, we use the following convention for naming `entity_id` for devices:

**General Structure:**
```
<location_code>_<device_code>_<function>_<identifier>
```

**Personal Devices:**
```
<user_code>_<device_type>_<identifier>
```

**Network Entities:**
```
<device_code>_<function>_<identifier>
```

_Where:_

- **`<location_code>`**: Indicates the specific location where the device is installed or controlled.
- **`<device_code>`** / **`<device_type>`**: Represents the type of device.
- **`<function>`**: Detail that provides additional information about the specific function of the device.
- **`<identifier>`**: Number or short name that distinguishes similar devices.
- **`<user_code>`**: Initials or nickname of the device owner.

**Examples of `entity_id`:**

- `kitchen_light_1` - The first light bulb installed in the kitchen.
- `bedroom1_thermostat_temperature` - Thermostat for temperature in the first bedroom.
- `garage_switch_door` - Switch for the garage door.
- `livingroom_sensor_motion` - Motion sensor in the living room.
- `bathroom_plug_heater` - Controlled outlet for the heater in the bathroom.

**For Personal Devices:**

- `john_main_phone` - John Doe's main mobile phone.
- `maria_apple_watch` - Maria Bianchi's Apple Watch.

**For Network Entities:**

- `fritzbox_connection_status` - Internet connection status of the Fritz!Box modem/router.
- `fritzbox_device_john_phone` - Fritz!Box network device associated with John Doe's mobile phone.

**Additional Notes:**

- It is important to document each newly added device according to this convention to maintain traceability and consistency.
- When applicable, use the location code where the device is located followed by the function it controls if it manages elements in another location (e.g., `gar_sw_garden_lights` for a switch in the garage that turns on garden lights).
- Use intuitive names and identifiers to simplify understanding and use of `entity_id`.

Use this documentation as a reference for adding new devices to your Home Assistant system, modifying the nomenclature as necessary to adapt to new situations or devices. Maintain an accessible and updated registry to facilitate scalability and maintenance of your home automation ecosystem.

---

Crafted by,
Your A.I. Home Assistant Guide Curator chatGPT (gpt-4-1106-preview)

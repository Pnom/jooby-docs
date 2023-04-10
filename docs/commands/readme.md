# Commands

There are 2 types of command direction:

- `downlink` - request (sent from server to device)
- `uplink` - response or event (sent from device to server)


## Downlink commands

 ID     | Name                                            | Description
--------|-------------------------------------------------|-------------
 `0x02` | [SetTime2000](./SetTime2000.md#request)         | Request to correct device time.
 `0x03` | [SetParameter](./SetParameter.md#request)       | Request to change device parameter.
 `0x0c` | [CorrectTime2000](./CorrectTime2000.md#request) | Request to correct device time by up to 127 seconds.
 `0x19` | [SoftRestart](./SoftRestart.md#request)         | Request to restart a device.


## Uplink commands

 ID     | Name                                             | Description
--------|--------------------------------------------------|-------------
 `0x02` | [SetTime2000](./SetTime2000.md#response)         | Response to the [SetTime2000](./SetTime2000.md#request) downlink command.
 `0x03` | [SetParameter](./SetParameter.md#response)       | Response to [SetParameter](./SetParameter.md#request) downlink command.
 `0x09` | [Time2000](./uplink/Time2000.md)                 | Current device time.
 `0x0c` | [CorrectTime2000](./CorrectTime2000.md#response) | Response to the [CorrectTime2000](./CorrectTime2000.md#request) downlink command.
 `0x16` | [DataDayMul](./uplink/DataDayMul.md)             | Pulse counter data of a multichannel sensor on billing hour.
 `0x17` | [DataHourMul](./uplink/DataHourMul.md)           | Pulse counter data of a multichannel sensor, accumulated on a hour basis.
 `0x18` | [GetCurrentMul](./uplink/GetCurrentMul.md)       | Current pulse counter value for multichannel devices.
 `0x19` | [SoftRestart](./SoftRestart.md#response)         | Response to the [SoftRestart](./SoftRestart.md#request) downlink command.
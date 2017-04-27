# Power Outlet

* `device.type`: `power-outlet`
* **Models**: No outlets currently supported
* **Model identifiers**: No outlets currently supported

Similar to the more generic type [`power-switch`](power-switch.md) but represents an outlet
mounted in or on a wall. Always has the capability
[`power-channels`](cap-power-channels.md) and can support more than one channel.

Supports the capabilities [`power-load`](cap-power-load.md)  and [`power-usage`](cap-power-usage.md).

## Basic API

### Properties

* `power`, array with the power state of all channels
* `powerChannelN`, where N is the channel (zero-indexed), boolean indicating if the channel is powered or not

### `device.channels: int`

The number of channels this device supports.

### `device.power(): Array[boolean]`

Get the powered on state of all channels as an array.

### `device.power(channel): boolean`

Get if the given channel is powered on.

### `device.setPower(channel, boolean): Promise`

Switch the power state of the given channel.
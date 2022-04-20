# Channels
- In golang, we can write and read to/from a single channel from multiple goroutines.
- But each goroutine will not read everything that is sent to the channel.
- Once the data from a channel is consumed by a goroutine, it is not available for consumption by the other goroutine. This does not work like pubsub, where duplicate read is possible

[back](https://github.com/manitejav/reading-material/blob/main/README.md#doc)

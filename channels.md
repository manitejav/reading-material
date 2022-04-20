[back](https://github.com/manitejav/reading-material/blob/main/README.md#doc)

# Channels
## Best practice
- prefer using formal arguments for the channels you pass to go-routines instead of accessing channels in global scope. You can get more compiler checking this way, and better modularity too.
- avoid both reading and writing on the same channel in a particular go-routine (including the 'main' one). Otherwise, deadlock is a much greater risk.

## Read and write
- In golang, we can write and read to/from a single channel from multiple goroutines.
- But each goroutine will not read everything that is sent to the channel.
- Once the data from a channel is consumed by a goroutine, it is not available for consumption by the other goroutine. This does not work like pubsub, where duplicate read is possible

[back](https://github.com/manitejav/reading-material/blob/main/README.md#doc)

# Noir MerkleRoot with Optimistic lookup table

I forked a noir example just to showcase the performance benefits of using a lookup table. This is a very bad implementation of using a lookup table. I am using the Noir standard types to implement a very bad table. We should expect to get better performance with a better implementation

Specs:
Fully specd Macbook pro bought in Jan2024
Apple M3 Max
128 GB

# Non-optimistic
On main branch you will find a normal merklization circuit (no optimistic table)
I get around a 1.97s proving time.

# Optimistic table
On 
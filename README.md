# Noir MerkleRoot with Optimistic lookup table

I forked a noir example just to showcase the performance benefits of using a lookup table. This is a very bad implementation of using a lookup table. I am using the Noir standard types to implement a very bad table. We should expect to get better performance with a better implementation

See: https://ethresear.ch/t/lookup-singularity-via-mmr/18704/6

Specs:
Fully specd Macbook pro bought in Jan2024
Apple M3 Max
128 GB

# Non-optimistic
On no-table branch you will find a normal merklization circuit (no optimistic table)
I get around a 1.97s proving time.

# Optimistic table
On main we have our new optimistic table scheme (poorly implemented). 

The proof takes around 0.385s

That is a 5.11x speedup with a really bad implementation.

# Verifying the table

When we use the optimistic table, the table is a public input of the proof we get.

We can have infrastructure verify the table on behalf of the user, in order to speed up mobile proof generation.

It takes me about 2s to verify the table we used optimistically. All of that is computation the user can avoid :)

# From this week onwards we will start the actual mining of data-blocks which is a computationally heavy task and the code might require some time to work as the nonce values could be very large.

### EXPLANATION OF ASSIGNMENT 5
In this assignment we will get a block from the user and we would have to carry out a lot of computations to calculate the nonce value for the block so that the target of the block header is less than the target value provided in the file. We will get a binary and we would have to read it so basically we have a task bit similar to assignment 4 and assignment 1.Also the Classes formed will be quite handy in managing the code for this week.

### APPLICATION SETUP
Run the following commands on your remote device to run the code -
```
git clone https://github.com/dkjha20/Blocks-and-Chains
cd 'Assignment 5'
npm install
```

### VARIOUS FILES CONTAINED

##### backend files not for the user -
1) - *package.json* - contains information of all Dependencies.
2) - *package-lock.json* - used for installation of all Dependencies on remote device using npm install command .
3) - *sample.dat* - file generated for testing of code .
4) - *block.dat* - file used for mining of the block .
5) - *extra.dat* - this is a extra file which is used by the efficient usage of mining algorithm.

##### source codes to be run -
6) - *mine.js* - this is the main code file which will ask for the input and give the corresponding nonce value and the timestamp as the output.

### EXAMPLES

1) -
run mine.js - input :
```
Index : 7
Hash of parent block: 41a82375fb23603aeb2129e6d05e2b4eb63b576db435f8e4ff2ad62ad4200fda
Target: 0000ffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff
Block Body: sample.dat
```

mine.js - output :
```
The appropriate set of nonce and time stamp is - 
NONCE VALUE -----  30556
TIMESTAMP -------  1627306893364
HASH OF BLOCK ---  0000beb9adea3bc5a60e09e7792118ab661d3377f1b4490b73f28150adb2c71a
Time consumed =    48.498291712 seconds
```

2) -

run mine_efficient.js - input :
```
Index : 7
Hash of parent block: 41a82375fb23603aeb2129e6d05e2b4eb63b576db435f8e4ff2ad62ad4200fda
Target: 00000f0000000000000000000000000000000000000000000000000000000000
Block Body: sample.dat
```

run mine_efficient.js - output :
```
NONCE VALUE -----  213320
TIMESTAMP -------  1627742238800
HASH OF BLOCK ---  00000944af025b846b0662c6bd504d4b5ed232077af53d0e6b5645beb8210c5b
Time consumed =    306.12249472 seconds
```

### EXTRAS

Though the mining work can be done by the file *mine.js* but I have made a bit more efficient algorithm which might be helpful in mining at a faster rate saving the time of writing the file again and again in the file *mine_efficient.js*.
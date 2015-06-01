# What can she do? #

  * Mark dangerous functions
  * Find immediate compares
  * Mark switches
  * Show paths between functions
  * Show paths between basic blocks within a function
  * Find File IO
  * Find Network IO
  * Find Allocations
  * Find dangerous „size params“

  * Create IDA (connection) graphs

  * Create „custom viewers“



# Details #

  * Mark dangerous functions
    * Look for references to "dangerous" functions within a binary and colour them for easy spotting.
    * For example: "call memcpy"
  * Find immediate compares
    * Mark all immediate compares in the current function. This is specially useful when analysing a huge function we suspect acts as a parser.
    * For example: cmp esi, 14h
  * Mark switches
  * Show paths between functions
  * Show paths between basic blocks within a function
  * Find File IO
    * Find functions calling file i/o imports.
  * Find Network IO
    * Find functions calling network i/o imports.
  * Find Allocations
    * Find functions allocating/freeing memory.
  * Find dangerous „size params“
    * Still a naive approach but interesting. Checks for calls to known problematic functions which accept a "size" parameter. If this argument is not a constant, it's worth it to take a look in case we can control it :)
  * Create IDA (connection) graphs
    * A class for creating IDA embedded Graphs, showing the paths between two functions and some other info.
  * Create „custom viewers“
    * Useful to display info (for example results of Find Network IO) in an embedded viewer within IDA Pro.
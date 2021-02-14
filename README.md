# Rigorous-2PL-Wound-Wait-Protocol

## Implementation of 2 phase locking with wound wait protocol.

I have implemented the 2PL protocol using **Java**. The implementation consists of three java files.

1. LockTable.java
2. Rigorous2PL.java
3. TransactionTable.java


### TransactionTable.java:

The TransactionTable class keeps track of the transactions that has been in process. This class has an arraylist to store the list of data items that is currently locked. There is a method **addBeginRecord()** which creates transaction_ID, timestamp of the transaction and the state of the transaction. This method is called when a new transaction comes into the system.

### LockTable.java:

The LockTable class is where the list of transctions that are currently holding the locks on the data item and the list of transactions that are waiting for the data item to be released by another transactions are stored. This class has a constructor that sets the lock status for each data item.

### Rigorous2PL.java:

The Rigorous2PL is the driver class for the entire application. The concept of wound-wait protocol has been implemented in this class. I have used FileReader to read the data items with its corresponding operations(*read*/*write*) to simulate the working of wound-wait protocol.



## Need of Builder Pattern : 
Method chaining is a useful design pattern but however if accessed concurrently, a thread may 
observe some fields to contain inconsistent values. Although all setter methods in above example 
are atomic, but calls in the method chaining can lead to inconsistent object state when the object 
is modified concurrently. The below example can lead us to a Student instance in an inconsistent state, 
for example, a student with name Ram and address Delhi.
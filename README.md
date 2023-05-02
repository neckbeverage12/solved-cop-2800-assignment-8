Download Link: https://assignmentchef.com/product/solved-cop-2800-assignment-8
<br>
When you go to the beach do you ever look up at the high rise condos?  I’ll bet those penthouse units belong to people with some serious money.  Let’s find out!

A thief breaks into a penthouse pad and collects valuables.  He doesn’t have a lot of time, so he might miss a few.  He throws them into his loot bag and rappels off the roof down to the street.  That’s a long way down!  On the way down, he drops his bag and those valuables that are breakable, like China, break.  When he gets home he estimates the value of the haul.

Design:

<ul>

 <li>An abstract class Valuable that has a dollar worth and a getter.</li>

 <li>Several subclasses of Valuable: Cash, Bond, Gold, China, Antique, Diamond, Jade, etc with toString methods.</li>

 <li>Select a few of the subclasses to implement this interface on.</li>

</ul>

interface Breakable {

void breakIt();

}

note: <em>break</em> is a Java keyword and can’t be used as a method name.(By the way, I think diamonds reputation for hardness is based on their resistance to scratching not cracking.  So, I made them Breakable, but you do as you please)




<ul>

 <li>Penthouse class that aggregates Valuables, can print out an inventory with currency format, and can relinquish a random number of Valuables.</li>

 <li>Thief class; really just a container for a LootBag.</li>

 <li>LootBag class that aggregates Valuables, can print out its contents, and can be dropped (in which case all the Breakable valuables break).</li>

</ul>




This is a pretty long program; your instructor’s was close to 200 lines including the driver.




Please title your java file Assignment8.java.  Submitted files that do not compile will receive a grade of 0.




Driver and sample output on next two pages:




public static void main (String [] arg) {

Penthouse GaltMile1  = new Penthouse();

GaltMile1.addValuable(new Diamond(10000));

GaltMile1.addValuable (new Bond(3000));

GaltMile1.addValuable (new Gold(20000));

GaltMile1.addValuable(new Antique(9000));

GaltMile1.addValuable (new China(4000));

GaltMile1.addValuable (new Cash(40000));

GaltMile1.addValuable (new China(2000));

GaltMile1.addValuable(new Antique(5000));

GaltMile1.inventoryValuables();




Thief itTakesA  = new Thief();

itTakesA.getBag().addLoot(GaltMile1.rob());

itTakesA.getBag().drop();




GaltMile1.inventoryValuables();

itTakesA.getBag().checkBag();

}







This line of code…




itTakesA.getBag().addLoot(GaltMile1.rob());




… represents the robbery.  It moves an array of Valuables from the Penthouse to the thief’s loot bag.  You are free to design this as you wish, but it’s the heart of the object transactions in the application.



1.Магнолија Огњановска 223181



2.![Final drawio](https://github.com/Magnolija10/SI_2024_lab2_223181/assets/164095051/6ba0a7ea-c81e-47c7-9392-7fa69d45cb8f)
3.Цикломатската комплексност на графот изнесува 10, бидејќи бројот на if-statements изнесува 7 и плус 2 за for циклусите кои имаат по еден предикат во себе, па така добиваме 9+1  според формулата, добиваме 10.
4.Според every-branch критериумот има 7 тест случаи:
     1. allItems==null - (го тестираме случајот каде 'allItems' e null, очекуваме да фрли exception : RuntimeEception ) 
     2. item==null i barcode so validno ime - (ги изминува гранките каде 'item.getName() == null' и 'item.getBarcode() != null', но со валидни карактери во баркодот, очекуваме : true )
     3. item so prazno ime i barcode so nevalidno ime - (ги изминува гранките каде 'item.getName().length() == 0' и 'item.getBarcode () != null' и 'allowed.indexOf(c) == -1' , очекуваме : RuntimeEception)
     4. item so barcode==null - (го покрива случајот каде 'item.getBarcode() == null'  , додека очекуваме : RuntimeEception)
     5. item so  popust, cena > 300 i barcode sto zapocnuva so '0' - (го поктива случајот каде имаме валиден barcode, cena >  300, popust > 0, и barcode кој започнува на 0, како резултат добиваме дополнително намалување на цената, очекуваме : true ) 
     6. suma < uplata - (го изминуваме случајот каде 'sum' е помала од 'payment' , очекуваме : true)
     7. suma > uplata - (го изминуваме случајот каде 'sum' е поголема од 'payment' , очекуваме : true)
5.Според multiple condition критериумот има 1 тест случај, низата ќе биде составена од 4 items 'if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0'':

 - сите услови се вистините (Т,Т,Т) Item1 = [new Item("item1", "0123456", 350, 0.1), 320)
 - првите два услови се вистинити, третиот е невистинит (Т,T,F) Item2 = [new Item("item1", "1123456", 350, 0.1)],
 - првиот услов е вистинит, вториот услов е невистинит, третиот услов е вистинит (T,F,T) Item3 = [new Item("item1", "0123456", 350, 0)],
 - првиот услов е невистинит, па затоа другите не се извршуваат (F,T,T) Item4 = [new Item("item1", "1123456", 250, 0.1)].

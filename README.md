# RTR180

Studiju kursa Datormācība (speckurss) elektroniskā klade.

## 2. nodarbības
rinda 1  

rinda 2  
rinda 3  

## 3. nodarbība







## 4. nodarbība
 
 OS? uname
 shell valodas stils/dialekts? echo -a
 Piemērs, bash
 
 Lietotājs vienmērs atrodas kādā failu sistēmas vietā. Mājas mapi apzīmē ar ~ .
 
 sh priekšrocība ir tā, ka tas patērē mazāk resursus, līdz ar to tas tiek plaši izmantots sistēmās,
 ar ierobežotiem atmiņas, jaudas vai citiem resursiem.

Lai no jebkuras mapes uzreiz nokļūtu uz mājas mapi lieto vienkārši cd

Komanda #!/bin/bash atļauj nano faila saturu interpretēt bin bash dialektā.

# Sistēmas ceļi

$PATH

PATH=PATH:(vajadzīgā mape) (skatīt nodarbības history)

PATH komanda parāda sistēmas ceļus, pa kuriem sistēma iet, lai meklētu izpildāmos failus.
Lietojot to nepareizi sistēmas ceļi var tikt  sajaukti, kā rezultātā komandas, kas strādāja vispirms vairs var nestrādāt. Šī problēma gan nav ilglaicīgi paliekoša problēma.

# Failu tiesību nomaiņa

Katram failam ir iespējami 3 tiesību veidi(read(r), write(w), execute(x))
Katra failam arī ir iespējams tiesību grupas(saimnieka tiesības, lietotāja tiesības, pārējo lietotāju tiersības)
Visām šim tiesību grupām ir iespējami arī visi tiesību veidi

Izmanto chmod

rwxr--r-- šajā piemērā ir parādīts, ka faila saimnieks ir tiesīgs uz read, write, execute tiesībām, faila lietojtājs ir tiesīgs uz read tiesībām, pārējie lietotāji arī ir tiesīgi tikai uz read tiesībām.

Ja grib nomainīt tiesības tad chmod (faila nosaukums) 750
Skaitļu vieta šajā 750 apzīmē tiesību grupas. Piemērā 7 ir pirmais no trim skaitļiem tāpēc tas apzīmē faila saimbnieka tiesības. Pārtaisot 7 no DEC uz BIN sanāk, ka 7 ir 111. Tas nozīmē, ka faila saimniekam ir atļautas visas tiesības (rwx). Līdzīgi ir ar 5 un 0.

Rezultāts ir:
rwxr-x---


##  5. nodarbība

  # Shell scripting tutorial
  
   Šeit apskata read cammand. Script paraugs
   
   #!bin/bash
   
    echo "What is your name?"
    read PERSON
    echo "Hello, $PERSON"
   
   Šeit read komandai tiek dots uzdevums nolasīt simbolus, kas tiek ievadīti PERSON vietā. Tas nozīmē, ka ja PERSON vietā būs  myname tad tiks atgriezts Hello, myname .
   
   
   # Shell Variables
   
   Shell parastie mainīgo apzīmējumi var saturēt burtus, ciparus vai underscore

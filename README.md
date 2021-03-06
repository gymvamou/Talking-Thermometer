# Talking-Thermometer
Θερμόμετρο χώρου για τυφλούς. 
Παρέχει φωνητικό μήνυμα της θερμοκρασίας για ανθρώπους που δεν μπορούν να διαβάσουν την ένδειξη σε μια οθόνη.
Έχοντας στο μυαλό μας ότι γύρω μας υπάρχουν αρκετοί άνθρωποι με ειδικές ανάγκες προσπαθήσαμε να βρούμε έναν τρόπο να τους βοηθήσουμε έτσι ώστε να απλοποιηθεί η ζωή τους σε κάποια καθημερινά ζητήματα τα οποία μπορεί να τους απασχολούν. Αποφασίσαμε λοιπόν, να απευθυνθούμε στην κατηγορία των τυφλών. Η έλλειψη όρασης αυτών των ανθρώπων δυσκολεύει πολύ την ζωή τους. Πολλές προειδοποιήσεις, λίστες, διαγνώσεις, ενδείξεις, κ.α. είναι γραμμένες, με αποτέλεσμα να μην υπάρχει τρόπος να τις «διαβάσουν». Το θερμόμετρο είναι ένα από τα πολλά αντικείμενα που έχουν φτιαχτεί για άτομα που έχουν την δυνατότητα να βλέπουν, άρα και να διαβάζουν. Όμως τι γίνεται με τους τυφλούς; Έτσι προσαρμόσαμε μια πολύ απλή συσκευή και καθημερινής χρήσης (το θερμόμετρο) πάνω στις ανάγκες των ατόμων αυτών. Θα χρησιμοποιήσουμε λοιπόν ηχητικά μηνύματα όπου ανάλογα με την θερμοκρασία του περιβάλλοντος που θα ανιχνεύει η συσκευή μας μέσω αισθητήρα θερμοκρασίας, θα αναπαράγει και το κατάλληλο για την περίσταση κλιπ ήχου το οποίο θα έχουμε ηχογραφήσει.
Πάνω σε ένα κουτί θα υπάρχει μια οθόνη στην οποία θα αναγράφεται η θερμοκρασία. Τις ενδείξεις αυτές θα τις λαμβάνει από έναν αισθητήρα θερμοκρασίας (DHT11) ο οποίος θα βρίσκεται κι εκείνος πάνω στο κουτί. Θα υπήρχαν ηχογραφημένα μηνύματα με τις ανάλογες θερμοκρασίες σε μια κάρτα μνήμης και ηχείo για να ακούγεται το μήνυμα. Όμως πως θα μπορούσε η συσκευή μας να «λέει» την θερμοκρασία την στιγμή ακριβώς που ο τυφλός θα ήθελε να την μάθει; Έτσι τοποθετώντας έναν αισθητήρα απόστασης (HC-SR04) θα πάρουμε το επιθυμητό αποτέλεσμα. Όταν ο τυφλός θέλει να μάθει την θερμοκρασία μπορεί να πηγαίνει απέναντι από την συσκευή και όταν βρεθεί σε απόσταση μικρότερη από 40cm τότε ο αισθητήρας απόστασης θα ενεργοποιεί μέσω του Arduino το κατάλληλο ηχητικό μήνυμα στην κάρτα SD. 
Μετά από αρκετή προσπάθεια δημιουργήσαμε κάτι ξεχωριστό, ένα θερμόμετρο για ανθρώπους που έχουν χάσει την όραση τους. 
Για την υλοποίηση του project χρησιμοποιούμε: ένα Arduino Uno, ένα  Breadboard, ένα Card Reader, μία LCD οθόνη, μερικά καλώδια, ένα αισθητήρα απόστασης, ένα αισθητήρα θερμοκρασίας, αντιστάτες, ηχείο και μία κάρτα micro SD. Αρχικά θα πραγματοποιήσουμε την σύνδεση των καλωδίων μεταξύ των Arduino, Card reader και Breadboard, στο οποίο θα τοποθετήσουμε τους αισθητήρες και τον αντιστάτη, ενώ στη συνέχεια θα ακολουθήσει και ο προγραμματισμός (επισυνάπτουμε ένα σχηματικό διάγραμμα των συνδέσεων που απαιτούνται). Στη συνέχεια συνδέσαμε την LCD Οθόνη και τo ηχείo. Έπειτα ηχογραφήσαμε μερικές τιμές της θερμοκρασίας που μπορεί να συναντήσει κανείς σε ένα σπίτι, τις μετατρέψαμε σε αρχείο τύπου wav σε 8bit και 16000Hz και τοποθετήσαμε τα αρχεία αυτά στην κάρτα SD. Στον προγραμματισμό ορίσαμε την απόσταση στην οποία θα ενεργοποιείται το φωνητικό μήνυμα και παράλληλα ορίσαμε το ποιο αρχείο θα παίζει ανάλογα με την θερμοκρασία που διαβάζει ο αισθητήρας θερμοκρασίας. Είναι αρκετά πολύπλοκο να συνδυαστούν οι εντολές αλλά ολοκληρώνοντας το project είμαστε ιδιαίτερα περήφανοι διότι αποτελεί μια καινοτομία. Υπάρχουν ήδη στο διαδίκτυο ξεχωριστά οι λειτουργίες αυτές (αναπαραγωγή αρχείου μέσω card reader, μέτρηση θερμοκρασίας, μέτρηση απόστασης, παρουσίαση τω μετρήσεων σε μια οθόνη LCD) αλλά πουθενά δεν υπάρχει ο συνδυασμός όλων των παραπάνω και έτσι χρειάστηκε να αυτοσχεδιάσουμε στη σύνδεση αλλά και στον προγραμματισμό του Arduino. Τέλος, αφού διαπιστώσουμε ότι λειτουργεί, ασχοληθήκαμε με την εξωτερική του εμφάνιση και βάλαμε το σύστημα μέσα σε μια όμορφη συσκευασία. Οι μαθητές που υλοποίησαν το project αυτό είναι οι: Κατερίνα, Μανώλης και Μαρία της Γ΄ τάξης του Γυμνασίου Βάμου (Χανίων). 

Το Video της παρουσίασης της κατασκευής στο κανάλι μας στο YouTube: 

https://www.youtube.com/watch?v=5MOvmwJ4jRM&feature=youtu.be


Υλικά που θα χρειαστούν:

1. Arduino UNO    7,50 €  
2. Breadboard     4,00 €  
3. micro SD  Card Reader  (Micro SD Storage Memory Board) 5,00 €  
4. micro sd card   8,00 €  
5. LCD (20x4) οθόνη  (I2C 20X4 Character LCD) 9,90 €
6. Αισθητήρας απόστασης (Ultrasonic Sensor HC-SR04 for Arduino) 2,00 €
7. Αισθητήρας θερμοκρασίας (DHT11 Digital Humidity Temperature Sensor for Arduino)  2,00 € 
8. καλώδια  3,50 €  
9. Υλικό για το εξωτερικό περίβλημα, το οποίο όμως δεν έχει καθοριστεί ακόμα.

συνολικό κόστος περίπου 42,00 € 

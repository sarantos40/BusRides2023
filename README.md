# BusRides 2023

Έργο για την βελτίωση της δημόσιας συγκοινωνίας

Στον 5ο ΠΑΝΕΛΛΗΝΙΟ ΔΙΑΓΩΝΙΣΜΟ ΑΝΟΙΧΤΩΝ ΤΕΧΝΟΛΟΓΙΩΝ ΣΤΗΝ ΕΚΠΑΙΔΕΥΣΗ

Πράσινη Οικονομία που θα είναι Ανοιχτή και Ιση για όλους

Μέσα μεταφοράς και πράσινη μετακίνηση

---

## Οι συγκοινωνίες

Η βελτίωση της κίνησης των μέσων μεταφοράς μπορεί να βελτιώσει την κίνηση των οχημάτων, την παραγωγή ρύπων και το περιβάλλον.
Η κεντρική ιδέα μας ήταν να γίνεται μετάδοση δεδομένων κίνησης από τα οχήματα (που προπορεύονται) και να την αξιοποιούν τα οχηματα που ακολουθούν για να κινηθούν πιο αποδοτικά.
Από τα κατάλληλα δεδομένα κίνησης τα οχήματα μπορεί να αποφασίσουν να αλλάξουν διαδρομή ώστε να ελαττωθεί η συμφόρηση. Αλλά και άλλες, μικρότερες, αποφάσεις μπορεί να είναι ουσιαστικές, και μάλιστα σε πιο εξειδευμένες κατηγορίες οχημάτων.
Μπορεί τα ταξί να χρησιμοποιήσουν πληροφορίες για το ποσοστό των ελεύθερων και γεμάτων ταξί στη διαδρομή, να αποφασίσουν την διαδρομή που θα ακολουθήσουν (όταν είναι ελεύθερα) για να βρουν με καλύτερη πιθανότητα μισθωτή.

## Τα λεωφορεία

Η μαζική μετακίνηση, με τα δημόσια μέσα μεταφοράς, μπορεί να ελαττώσει την άσκοπη κατανάλωση ενέργειας.
Όπως για να είναι πιο μαζική και αποτελεσματική πρέπει να είναι και εξυπηρετική προς τους επιβάτες.

Εμείς θα ασχοληθούμε με λεωφορεία: Τα λεωφορεία δεν αλλάζουν διαδρομή, και η κίνηση στους δρόμους τα επηρρεάζει περισσότερο. Συχνά σε περιόδους μεγάλης κίνησης καθυστερούν, αλλα η κυκλοφορία δεν είναι σταθερά πιο αργή - και μπορεί το πίσω λεωφορείο να προλάβει το μπροστινό, οπότε δεν προσφέρει κάποια πρόσθετη εξυπηρέτηση. 
Όταν δύο λεωφορεία της ίδιας διαδρομής κινούνται κοντά, το πρώτο συνήθως έχει μεγαλύτερη πληρότητα και καθυστερεί περισσότερο στις στάσεις για αποβίβαση και επιβίβαση (καθώς έχουν ήδη μαζευτεί περισσότεροι επιβάτες στο λεωφορείο και σε κάθε στάση). Έτσι σιγά σιγά το δεύτερο λεωφορείο πλησιάζει περισσότερο το πρώτο - και το πρόβλημα της κίνησης σε κοντινή απόσταση γίνεται πιο έντονο. Οπότε το πρόβλημα χειροτερεύει αντί να αυτορυθίζεται.

Η καλύτερη εξυπηρέτηση των επιβατών προκύπτει όταν (μέσα την κίνηση και καθυστέρηση που δεν μπορούμε να αποφύγουμε) τα λεωφορεία διέρχονται από τη διαδρομη (και τις στάσεις) σε ισαπέχοντα χρονικά διαστήματα. Και αυτό, ως κάποιο βαθμό, μπορεί να το ρυθμίσει ο οδηγός - αποφασίζοντας αν θα καθυστερήσει παραπάνω στη διαδρομή (οδηγόντας οικονομικά) και στις στάσεις, ή αν θα προσπαθήσει να καλύψει χρόνο τρέχοντας ή κάνοντας προσπεράσεις (π.χ. άλλων λεωφορείων).

## Το έργο μας

Στο έργο μας θα χρήσιμοποιήσουμε 2 οχήματα: το μπροστινό λεωφορείο θα κινείται (βασική μονάδα ένα microbit) πάνω στην προκαθορισμένη διαδρομή του και θα επιτηρεί τη διαδρομή του και τα εμπόδια (με αισθητήρα όρασης HuskyLens) τροποποιώντας αντίστοιχα την ταχύτητά του. Με βάση αυτά θα δίνει (ασύρματα, με το microbit του) στοιχεία στο λεωφορείο που ακολουθεί στην ίδια διαδρομή.
Το λεωφορείο που ακολουθεί θα λαμβάνει τα στοιχεία (με το δικό του microbit), θα τα αξιολογεί και θα τα συνδυάζει με τα αμετάβλητα στοιχεία της διαδρομής, ώστε να αναθεωρεί το στόχο του για τις ώρες άφιξης.
Έτσι τελικά θα αποφασίζει πόσο θα μεταβάλει την ταχύτητά του για να είναι κοντά στο στόχο του.

Τα οχήματα θα έχουν επικοινωνία και με κεντρικό σταθμό - σταθμαρχείο (ασύρματα, με microbit),
για αποστολή πληροφορίας για την κίνησή τους και λήψη οδηγιών από αυτό.
Το σταθμαρχείο θα περιλαμβάνει gamepad για να μπορεί να δίνει οδηγίες στα οχήματα.

## Περιβάλλον ανάπτυξης

Επιλέκτηκε η πλατφόρμα του microbit, καθώς έχει τη δυνατότητα να καλύψει όλα τα μέρη του σχεδιασμού,
τη συνδεσμολογία τους (φυσική ή ασύρματη) χωρίς να γίνεται πολύ γενική (όπως με την υπολογιστική ισχύ του raspberry pi).
Όλα τα εξαρτήματα υποστηρίζονται από το λογισμικό makecode και το mindplus, με υπάρχουσες επεκτάσεις.
Μπορεί όμως να υπάρχουν ασυμβατότητες στη χρήση των διαφορετικών επεκτάσεων, και να εφαρμόσουμε εναλλακτικό σχέδιο.
Θα χρησιμοποιηθεί (αρχικά τουλάχιστον) το makecode. Εναλλακτικά, το mindplus.
Βλέποντας τα περιβάλλοντα αυτά, θα έπρεπε και τα δύο να υποστηρίζουν τη λειτουργικότητα που θέλουμε.
Αν υπάρχουν πολλές ασυμβατότητες, θα προσπαθήσουμε να καταφύγουμε σε python.

## Υλικά και προϋπολογισμός

Θα χρησιμοποιηθούν 2 maqueen (έτοιμα) οχήματα με microbit ως λεωφορεία
και ένα ακόμα microbit για το σταθμαρχείο.
Το πρώτο όχημα θα έχει και αισθητήρα HuskyLens για να ανιχνεύει εμπόδια.
Το σταθμαρχείο θα έχει χειριστήριο για αποστολή εντολών στα οχήματα
και βάση για να μπορεί επίσης να συνδεθεί (πειραματικά τουλάχιστον) με άλλες συσκευές.

## Η κύρια πρόκληση - η επικοινωνία

Η κύρια ιδέα του έργου είναι
η ανάπτυξη πρωτοκόλλου ασύρματης ανταλλαγής της απαιτούμενης πληροφορίας,
που πρέπει να κατανοήσουμε και απομονώσουμε την ουσιαστική πληροφορία,
να την κωδικοποιήσουμε κατάλληλα, και να την αποστείλουμε.
Αντίστοιχα, όταν την λαμβάνουμε πρέπει να την ερμηνεύσουμε,
να την αξιοποιήσουμε κατάλληλα
και να προσαρμόσουμε την κατάστασή μας.

Η επικοινωνία θα ξεκινά και θα λαμβάνεται οποιοαδήποτε στιγμή,
παράλληλα με την φυσιολογική λειτουργία των οχημάτων,
και δεν θα είναι απλώς διμερής, καθώς θα υπάρχει και το σταθμαρχείο,
ενώ θα είναι αμφίδρομη,
καθώς όλοι θα λαμβάνουν και θα στέλνουν με δική τους πρωτοβουλία.

Η ανταλλαγή πληροφορίας κίνησης,
μαζί με όλες τις εντολές και πληροφορίες που ανταλλάσσονται,
πρέπει να σχεδιαστούν κατάλληλα,
ώστε να συνυπάρχουν στην επικοινωνία
και να διαχωρίζονται σωστά.

## Οι επιμέρους προκλήσεις

Μέσω του έργου αυτού θα πειραματιστούμε με:

* Αυτόνομη οδήγηση οχήματος (πιθανότατα ακολουθώντας μια γραμμή)
* Χρήση εικόνας Huskylens για AI
* Ανίχνευση και αντίδραση σε εμπόδια πάνω στη διαδρομή, σταθερά ή κινητά
* Αποτύπωση των καθυστερήσεων της διαδρομής σε πληροφορία
* Ασύρματη αποστολή της πληροφορίας
* Ασύρματη λήψη της πληροφορίας
* Ερμηνεία της πληροφορίας και συνδυασμό της με τα δεδομένα της διαδρομής
* Πρόβλεψη της ταχύτητας του οχήματος
* Προσαρμογή της ταχύτητας του οχήματος για να πλησιάσει την επιθυμητή.
* Αποστολή εντολών από το σταθμαρχείο στα οχήματα
* Λήψη πληροφοριών κίνησης από το σταθμαρχείο (ή και άλλους πίνακες), για να τις εμφανίζει στην οθόνη

Επίσης, πιθανότατα θα χρειαστεί να ασχοληθούμε με:

* αρχική εκπαίδευση της διαδρομής για αυτόματη καταγραφή / χαρτογράφηση των δεδομένων.
* υιοθέτηση κυκλικής πορείας / διαδρομής
* εμφάνιση κατάλληλων ενδείξεων και πληροφορίας διαδρομής στην οθόνη
* ανίχνευση των στάσεων
* θα κάνει στάσεις με τυχαιοποιημένη διάρκεια
* δοκιμές με διαφορετικές ταχύτητες κίνησης
* σύνδεση επιπλέον συσκευών στο σταθμαρχείο
* χρήση παραπάνω σταθμών ελέγχου - σταθμαρχείων
* επαναποστολή πληροφορίας όταν αυτή χάνεται

## Παραλλαγές του έργου

Ένα μικρότερο έργο θα μπορούσε να περιοριστεί στα 2 οχήματα, χωρίς το σταθμαρχείο, την ανταλλαγή απλής πληροφόρησης και την αποστολή άμεσων εντολών στα οχήματα.

Σε πιθανή κλιμάκωση του προβλήματος θα μπορούσαν να χρησιμοποιηθούν:
* περισσότερα οχήματα (όπως ένα λεωφορείο πιο πίσω, και απόσταση από αυτό),
* περισσότερα δεδομένα κίνησης (ακόμα και αλλων ημερών ή άλλων οχημάτων), προβλέψεις για την κίνηση που θα συναντήσουν, στοιχεία πληρότητας των λεωφορείων, κ.α.
* χρήση πληροφορίας από άλλες πηγές, π.χ. δρόμου (φανάρια κυκλοφορίας, κ.α.)
* μεγαλύτερη εμπλοκή του κεντρικού σταθμού (σταθμαρχείου) στην κίνηση των οχημάτων, με περισσότερες εντολές και μεγαλύτερο έλεγχο, με καλύτερη διεπαφή με το χρήστη.

Σε άλλες παραλλαγές, τα οχήματα (ειδικά αν δεν ήταν λεωφορεία ή τρένα -π.χ. ταξί, οχήματα εφοδιασμού καταστημάτων, κ.α.) θα μπορούσαν να αλλάζουν και διαδρομή, με κατάλληλες οδηγίες πλοήγησης.
Και στα λεωφορεία, θα μπορούσαν μερικά οχήματα (π.χ. ένα παρά ένα) να αλλάξουν διαδρομή παραλείποντας δρόμους και στάσεις, για την καλύτερη εξυπηρέτηση των επιβατών που βρίσκονται σε ζώνη μικρής κυκλοφοριακής επιβάρυνσης, μη περνώντας τους από τους συνωστισμένους δρόμους.

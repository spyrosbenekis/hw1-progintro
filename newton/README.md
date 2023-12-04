Το πρόγραμμα χρησιμοποιεί δύο συναρτήσεις και μια αναδρομή τις:

1.  double f(double xn)

    Η συνάρτηση f δέχεται σαν όρισμα την τιμή του σημείου xn και επιστρέφει την τιμή της πολυωνυμικής συνάρτησης στο σημείο xn. Αυτό γίνεται με την χρήση του βρόχου, που προστείθετε κάθε φορά στην μεταβλητή η τιμή της συνάρτησης στην αντίστοιχη δύναμη.

2.  double factor(double xn)

    Η συνάρτηση factor δέχεται σαν όρισμα την τιμή του σημείου xn και επιστρέφει την τιμή της παραγώγου στο σημείο xn. Αυτό γίνεται με την χρήση του βρόχου, που προστείθετε κάθε φορά στην μεταβλητή η τιμή της συνάρτησης στην αντίστοιχη δύναμη μειωμένη κατά 1 και πολλαπλασιασμένο με το αντίστοιχο i (όπως γίνεται κάθε φορά που παραγωγίζουμε μια συνάρτηση όπου η δύναμη "πέφτει" και πολλαπλασιάζεται με τον συντελεστή ενώ η δύναμη μειώνεται κατά ένα). Στο τέλος, αφού έχει υπολογιστεί η τιμή της παραγώγου, ελέγχεται αν η απόλυτη τιμή της -με την χρήση της συνάρτητηση fabs που επιστρέφει την απόλιτη τιμή του αριθμού- συγκλίνει στο μηδέν. Αν αυτό ισχυεί τότε η συνάρτηση επιστρέφει μηδέν, αλλιώς επιστρέφει την τιμή της παραγώγου.

3.  void newton(double xn)

    Η αναδρομή newton χρησιμοποιείται για να υπολογιστεί η ρίζα της πολυωνυμιακής συνάρτησης. Αρχικά με την εντολή 
    fac = factor(xn), αποθηκεύεται -με την κλήση της συνάρτησης- η τιμή της παραγώγου στο σημείο στην μεταβλητή fac. Μετά, με τις δύο πρώτες συνθήκες ελέγχετε αν ο αλγόριθμος πρέπει να τερματιστεί με βάση τις περιπτώσεις που αναφέρονται στην εκφώνηση. Αν δεν είναι ισχύει κάποια από τις δύο περιπτώσεις, τότε γίνετε προσπάθεια υπολογισμόυ τις ρίζας -με βάση τον τύπο που δίνετε από την εκφώνηση. Σε περίπτωση που το xn1 που βρέθηκε συγκλίνει, δηλαδή ισχύει ότι |xn+1 − xn| < 10^−6, τότε εκτυπώνει το xn1. Αλλιώς ξανά καλείται αναδρομικά η συνάρτηση newton με νέα τιμή το xn1 που έχει βρεθεί (ώστε στην επόμενη εκτέλεση να προσεγγιστεί περισσότερο η ρίζα). Για τον έλεγχω του πλήθους των εκτελέσεων της αναδρομής χρησιμοποιείται η καθολική μεταβλητή count, της οποίας το πλήθος σε κάθε εκτέλεση της αναδρομής αυξάνεται κατά ένα.

Στην main αρχικά ελέγχω το πλήθος των ορισμάτων και στην συνέχεια τα αποθηκεύω σε έναν πίνακα καθολικής εμβέλειας, ώστε να μπορεί να χρησιμοποιθεί και από τις άλλες συναρτήσεις και για να μην χρειάζεται να τον δέχονται κάθε φορά σαν όρισμα. Τέλος, καλείται η συνάρτηση netwon και εφόσον όλα εκτελούνται χωρίς προβλήματα, επιστρέφεται η τιμή μηδέν.
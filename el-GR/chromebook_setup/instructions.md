Μπορείτε [ να παραλείψετε αυτή την ενότητα](http://tutorial.djangogirls.org/en/installation/#install-python) εάν δεν χρησιμοποιείτε το Chromebook. Εάν το χρησιμοποιείτε, η διαδικασία εγκατάστασης θα είναι λίγο διαφορετική. Σε αυτή την περίπτωση μπορείτε να αγνοήσετε τις υπόλοιπες οδηγίες εγκατάστασης.

### Cloud IDE (PaizaCloud Cloud IDE, AWS Cloud9)

Το CloudIDE είναι ένα εργαλείο το οποίο σου παρέχει έναν επεξεργαστή κώδικα καθώς και πρόσβαση σε έναν υπολογιστή στο internet στον οποίο μπορείς να εγκαταστήσεις, να γράψεις και να τρέξεις το λογισμικό. Κατά τη διάρκεια του οδηγού, το CloudIDE θα παίζει το ρόλο του *local machine* (δηλαδή του τοπικού υπολογιστή σας). Παραταύτα, θα χρειαστεί να γράφετε εντολές στο τερματικό όπως ακριβώς οι συμμαθητές σας που χρησιμοποιούν OS X, Ubuntu ή Windows, με την μόνη διαφορά ότι το τερματικό δεν θα τρέχει στον υπολογιστή που κάθεστε αλλά στο cloud (σύννεφο), εκεί που το όρισε το CloudIDE (σε κάποιον εικονικό υπολογιστή, δηλαδή, στο internet). Εδώ είναι οι οδηγίες για τα cloud IDEs (PaizaCloud Cloud IDE, AWS Cloud9). Μπορείτε να επιλέξετε ένα από τα cloud IDEs και να ακολουθήσετε τις αντίστοιχες οδηγίες του.

#### PaizaCloud Cloud IDE

1. Πηγαίνετε στο [PaizaCloud Cloud IDE](https://paiza.cloud/)
2. Δημιούργησε λογαριασμό
3. Κάντε κλικ στο κουμπί *New Server*
4. Κάντε κλικ στο κουμπί Terminal (στην αριστερή πλευρά του παραθύρου)

Τώρα θα πρέπει να δείτε μια σελίδα με πλαϊνή μπάρα εργασίων και κουμπιά στα αριστερά. Κάντε κλικ στο κουμπί «Terminal» για να ανοίξετε το παράθυρο του τερματικού (ή αλλιώς "κοσνόλα" ή "γραμμή εντολών") όπως παρακάτω:

{% filename %}Terminal{% endfilename %}

    $
    

Το τερματικό στο PaizaCloud Cloud IDE είναι έτοιμο να δεχτεί τις εντολές σας. Μπορείτε να αλλάξετε το μέγεθος του παραθύρου ή να το μεγιστοποιήσετε, αν θέλετε.

#### AWS Cloud9

1. Μεταβείτε στο [AWS Cloud9](https://aws.amazon.com/cloud9/)
2. Δημιούργησε λογαριασμό
3. Κάντε κλικ στο κουμπί *Create Environment*

Τώρα θα πρέπει να δείτε μια σελίδα με πλαϊνή μπάρα εργασίων, ένα μεγάλο κύριο παράθυρο με κείμενο και ένα μικρό παράθυρο στο κάτω μέρος της που μοιάζει κάπως έτσι:

{% filename %}bash{% endfilename %}

    yourusername:~/workspace $
    

This bottom area is your terminal. You can use the terminal to send instructions to the remote Cloud 9 computer. You can resize that window to make it a bit bigger.

### Εικονικό Περιβάλλον

Το εικονικό περιβάλλον (επίσης και ως virtualenv - virtual environment) είναι σαν ένα κουτί όπου μπορούμε να βάλουμε μέσα κώδικα για ένα project χωρίς αυτό να αλληλεπιδρά με κώδικα του συστήματος. Τα χρησιμοποιούμε ούτως ώστε κάθε project να έχει τα δικά του κομμάτια κώδικα και έτσι επιτυγχάνουμε απομόνωση των projects. Φανταστείτε να είχατε ένα project που εξαρτάται από την έκδοση Django 2.0 και ένα άλλο που εξαρτάται από το Django 2.1. Πως θα ικανοποιούσατε τις απαιτήσεις κάθε project; Η απάντηση είναι τα virtualenvs!

Στο τερματικό σας στο κάτω μέρος, γράψτε τα εξής:

{% filename %}Cloud 9{% endfilename %}

    sudo apt update
    sudo apt install python3.6-venv
    

Αν αυτό εξακολουθεί να μην λειτουργεί, θα πρέπει να ζητήσετε βοήθεια από κάπου.

Στη συνέχεια, τρέξτε τις ακόλουθες εντολές:

{% filename %}Cloud 9{% endfilename %}

    mkdir djangogirls
    cd djangogirls
    python3.6 -mvenv myvenv
    source myvenv/bin/activate
    pip install django~={{ book.django_version }}
    

(παρατήρησε ότι στην τελευταία γραμμή χρησιμοποιούμε μία περισπωμένη, την οποία ακολουθεί ένα ίσον: ~=).

### GitHub

Φτιάξε έναν λογαριασμό στο [GitHub](https://github.com).

### PythonAnywhere

Ο οδηγός της κοινότητας Django Girls περιλαμβάνει μια ενότητα αυτού που ονομάζεται Deployment (δυστυχώς δεν υπάρχει κάποιος ακριβής ελληνικός όρος, οπότε θα αναφερόμαστε σε αυτόν με την αγγλική λέξη) που είναι η δυνατότητα του να "ανεβάσεις" τον κώδικα σου - αυτόν που είναι γραμμένη η εφαρμογή σου - σε κάποιον διακομιστή (server) ο οποίος είναι προσβάσιμος από όλους, ούτως ώστε οι άλλοι να δουν τη δουλειά σας.

Αυτό το κομμάτι είναι λίγο περίεργο όταν ακολουθείτε αυτόν τον οδηγό σε ένα Chromebook, δεδομένου ότι χρησιμοποιείτε ήδη έναν υπολογιστή που βρίσκεται στο διαδίκτυο (σε αντίθεση με την περίπτωση του φορητού ή επιτραπέζιου υπολογιστή). Ωστόσο, θεωρείται ακόμα χρήσιμος ο όρος αυτός (deployment), καθώς μπορούμε να αναλογιστούμε το χώρο εργασίας του Cloud 9 ως το «προς εξέλιξη έργο» και την εταιρεία PythonAnywhere ως ένα μέρος για να "ανεβάσουμε" την εργασία μας καθώς αυτή θα ολοκληρώνεται.

Δημιουργήστε λοιπόν έναν νέο λογαριασμό στο PythonAnywhere ακολουθώντας αυτόν τον σύνδεσμο [www.pythonanywhere.com](https://www.pythonanywhere.com).
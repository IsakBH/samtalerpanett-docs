# Database include fil
Database include filen, som vi har kalt `db.inc.php`, ser slik ut:
```php
<?php
$db_server = ""; // f.eks 'localhost'
$db_user = ""; // f.eks 'isak'
$db_pass = ""; // f.eks 'passord01' (plis ikke)
$db_name = ""; // f.eks samtalerpanett
$conn = ""; // denne blir tom - variabelen blir bare declared her

$protocol = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] !== 'off') ? 'https' : 'http';
$websocket_protocol = "ws";
$wshostname = $_SERVER['host'];
$wsport = 8080;
$wsroute = "/chat";

$conn = mysqli_connect($db_server, $db_user, $db_pass, $db_name);
if (!$conn) {
    die("Connection failed: " . mysqli_connect_error());
}

function dbConnection()
{
    $db_server = ""; // f.eks 'localhost'
    $db_user = ""; // f.eks 'isak'
    $db_pass = ""; // f.eks 'passord01' (plis ikke)
    $db_name = ""; // f.eks samtalerpanett
    $conn = "";

    $conn = mysqli_connect($db_server, $db_user, $db_pass, $db_name);
    if (!$conn) {
        die("Connection failed: " . mysqli_connect_error());
    }

    return $conn;
}
```

Dette er hvordan min ser ut, og jeg anbefaler at det er sånn din ser ut. All koden som er skrevet er skrevet basert på dette her, så variabel navnene må være lik, men strukturen trenger selvfølgelig ikke være det.

*Noe å notere: variablene `wshostname`, `wsport` og `wsroute` het det samme før men uten 'ws'. Plis bruk disse variabelnavnene. Jeg vil veldig gjerne at setupet jeg har på serveren her er identisk setupet til alle contributors i Git - det gjør livet mitt så sykt mye lettere.*
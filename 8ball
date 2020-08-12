<?php

Class Magic8Ball{
    
    public $q;

    public function __construct($q){
        $this->q = $q;
    }

    public function answers(){
        $answers = array("As I see it, yes.",
        "Ask again later",
        "Better not tell you now",
        "Cannot predict now",
        "Concentrate and ask again",
        "Don't count on it",
        "It is certain",
        "It is decidedly so",
        "Most likely",
        "My reply is no",
        "My sources say no",
        "Outlook not so good",
        "Outlook good",
        "Reply hazy, try again",
        "Signs point to yes",
        "Very doubtful",
        "Without a doubt",
        "Yes",
        "Yes - definitely",
        "You may rely on it");

        $randAns = array_rand($answers);
        $result = '<div class="alert alert-dark" style="border:1px solid black;background-image: linear-gradient(to right, black,black,#0E14CF,#0E14CF,black,black);"><strong style="font-size:21px;color:white;">' . $answers[$randAns].'</strong></div>';
        return $result;
    }

} // End class
?>
<!-- End of PHP -->


<!DOCTYPE html>
<html>
    <head>

    <title>Magic 8 Ball</title>
    <title>Calculator</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">

    <!-- jQuery library -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

    <!-- Latest compiled JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>

</head>
<body style = "background-color:black">

<br><br>

<div class = "container">
    <div class = "row">
        <div class = "col-lg-12" style = "text-align:center">
            <h1 style = "color:white; font-family:cursive">Magic 8 Ball</h1>
            <br><br>
            <img src = "8ball.png">

            <!-- PHP -->
            <?php

            if(isset($_POST['ask'])){
                $q = $_POST['question'];

                $ans = new Magic8Ball($q);
                echo $ans->answers();
            }

            ?> 
            <!-- End of PHP -->

            <form action = "index.php" method = "POST">

                <input type = "text" name = "question" placeholder = "Ask a yes or no question" style = "width:1000px; height:50px; font-family:cursive; color:blue; font-size: 24px" required oninvalid="setCustomValidity('This ball is not a mind reader! Fill out a question!')" oninput="this.setCustomValidity('')"><br><br>

                <button name = "ask" style = "width:200px; background-color:blue; color:white; font-family:cursive; height:75px; font-size:24px">Ask the Magic 8 Ball</button><br><br>
</form>
</body>
</html>

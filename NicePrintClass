<?php
function prettyPrint($array,$deep = 0){
    $intendation = "&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;";
    $lastElement = end($array);
    foreach($array as $key=>$value) {
        if($deep>0) {
            for($i=0;$i<$deep;$i++) {
                echo  $intendation;
            }
            echo $key . " => " . $value . "<br>";
        } else {
            echo $key . " => " . $value . "<br>";
        }
        if(is_array($value)) {
            $deep++;
            prettyPrint($value,$deep);
            if($key == $lastElement) {
                $deep = 0;
            } else {
                $deep--;
            }
        }
    }
}

$array = ["item1"=>"432","item2"=>"3454","item3"=>
    ["prop1"=>123,"prop2"=>"454556","prop3"=>
        ["2","3","prop3"=>
            ["2","3","prop3"=>
                ["2","3","4"],
                "prop4"=>
                ["2","3","4"],
                "prop5"=>
                ["2","3","4"]
            ]
        ]
    ],
    "item4"=>["prop1"=>235,"prop2"=>"ssferrr"]];


prettyPrint($array);

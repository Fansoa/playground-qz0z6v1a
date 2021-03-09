<?php
class SelectCreator{

    public $_opTag = '<select>';
    public $_endTag = '</select>';

    public function __construct(int $_nbrOptions){
        $this->_nbrOptions = $_nbrOptions;
    }

    public function inputSelect(){
        $string = $this->_opTag;
        for ($x = 1; $x <= $this->_nbrOptions; $x++){
            if ($x%2 == 1){
                $string .= "<options value=\"$x\">$x impair</options>";
            }
            else {
                $string .= "<options value=\"$x\">$x pair</options>";
            }
        }
        $string .= $this->_endTag;
        echo $string;
    }
}
$class = new SelectCreator(8);
$class->inputSelect();
//var_dump($string)
?>

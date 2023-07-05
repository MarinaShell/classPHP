<?php

interface TechnicInterface
{
    /*движение вперед*/
    public function moveForward(); 

    /*движение назад*/
    public function moveBack(); 
}

abstract class TechnicClass implements TechnicInterface 
{  
    /*движение вперед*/
    public function moveForward()
    {
        echo "moveForward\n";
    } 

    /*движение назад*/
    public function moveBack()
    {
        echo "moveBack\n";
    } 
 }

 /*класс машин*/
class Cars extends TechnicClass
{
    /*цвет машины*/
    private $color = "WHITE";  
    private $signal = false;
    private $isWipe = false;

    /*распечатать цвет  */
    private function makeColor()
    {
        echo $this->color;
    }

    /*цвет для машины*/
    public function setColor(string $color)
    {
        $this->color = $color;
        $this->makeColor();
    }

    /*способность сигналить*/
    public function setSignal(bool $isSignal)
    {
        $this->signal = $isSignal;
    }

    /*вклюсить дворники*/
    public function onWipers(bool $isWipe)
    {
        $this->isWipe = $isWipe;
    }    

}

/*класс танков*/
class Tanks extends TechnicClass
{
    /*размер пушки*/
    private $shoot = 100;  

    /*стрелять из пушки*/
    private function makeShoot()
    {
        echo $this->shoot;
    }

    /*размер пушки*/
    public function setShoot(int $shoot)
    {
        $this->shoot = $shoot;  
        $this->makeShoot();
    }
}

/*класс спецтехники*/
class Spectechnic extends TechnicClass
{
   /*размахивать ковшом*/
    public function makeMoving()
    {
        echo "makeMoving";
    } 
}

$tech = new Cars();
//$tech = new Tanks();
//$tech = new Spectechnic();
// функция с явным указанием типа (родительского типа)
function testCars(TechnicInterface $tech)
{
  $tech->moveForward();
  $tech->moveBack();
  if (is_a($tech, 'Cars'))
  {
    $tech->setColor('RED');
    $tech->setSignal(true);
    $tech->onWipers(true);  
  }

  if (is_a($tech, 'Tanks'))
  {
    $tech->setShoot(200);
  }

  if (is_a($tech, 'Spectechnic'))
  {
    $tech->makeMoving();
  }
}

 testCars($tech);
?>

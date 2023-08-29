1-)
<?php 
class Car {
    private $model;

    public function setModel($model) {
        $this->model = $model;
    }

    public function getModel() {
        return $this->model;
    }
}

$car = new Car();
$car->setModel("Toyota");
echo $car->getModel(); // Output: Toyota

?>

2-)
<?php 
class Person {
    private $name;
    private $age;

    public function setName($name) {
        $this->name = $name;
    }

    public function getName() {
        return $this->name;
    }

    public function getAge() {
        return $this->age;
    }
}

$person = new Person();
$person->setName("John");
echo $person->getName(); // Output: John
echo $person->getAge();

?>

3-)
<?php 
class Calculator {
    public function add($a, $b) {
        return $a + $b;
    }

    public function subtract($a, $b) {
        return $a - $b;
    }
}

$calculator = new Calculator();
echo $calculator->subtract(2, 3);

?>

4-)
<?php 
class Math {
    public function divide($a, $b): float {
        return $a / $b;
    }
}

$math = new Math();
echo $math->divide(10.5, 2);

?>

5-)
<?php 
class BankAccount {
    private $balance;

    public function deposit($amount) {
        $this->balance += $amount;
    }

    public function withdraw($amount) {
        if ($amount <= $this->balance) {
            $this->balance -= $amount;
        } else {
            echo "Insufficient balance.";
        }
    }

    public function getBalance() {
        return $this->balance;
    }
}

$account = new BankAccount();
$account->deposit(100);
$account->withdraw(50);
echo $account->getBalance(); 

?>

6-)
<?php 
class StringUtils {
    public static function concatenate($str1, $str2) {
        return $str1 . $str2;
    }
}

echo StringUtils::concatenate("Hello"," World"); // Output: Warning: Missing argument 2 for StringUtils::concatenate()

?>

7-)
<?php 
class DiscountCalculator {
    private $minimumValue = 10;
    public function calculateDiscount($amount) {
        
        if ($amount > $this->minimumValue) {
            $discount = $amount * 0.1;
        } else {
            $discount = $amount * 0.05;
        }
        
        // Algum código adicional que altera o valor mínimo durante a validação
        $this->minimumValue = 20;
        
        return $discount;
    }
}
$DiscountCalculator = new DiscountCalculator();
echo $DiscountCalculator->calculateDiscount(400);

?>


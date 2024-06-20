---
title: Interface
date: 2024-06-20 07:00:00 +0700
categories: ["Learn, IT"]
tags: ["Learn, IT, OOP"]
---

# Mình đã quay trở lại đây

Bài học hôm nay, bãi học vỡ lòng mà bây giờ tôi mới hiểu ra. Cho dù thế nào thì cũng lên biết những thứ cơ bản trước đúng không.

# Interface 
Cứ nhắc đến interface là chúng ta (các bạn lập trình viên ^^), nghĩ ngay đến OOP (lập trình hướng đối tượng). Vậy intarface là gì? Nó có liên quan gì đến các đối tượng.

# Interface là gì?
Để hiểu đơn giản, interface giống như 1 bản thiết kế. Trong xây dựng, luôn phải tạo sẵn 1 bản thiết kế, cung cấp các thông số kỹ thuật để triển khai, bên nhân công họ sẽ triển khai theo bản thiết kế có sẵn đó.

Tương tự, trong lập trình, interface là **thiết kế cho các lớp**. Nó chỉ định phương thức triển khai, mà không chứa bất kỳ logic xử lý nào. Interface chỉ khai báo phương thức và không có nội dung bên trong phương thức.

## Tính chất hướng đối tượng của interface.
- Đó chính là tính chất **trừu tượng**

## Ví dụ minh họa

    <?php
    
    // Tính trừu tượng
    // Định nghĩa interface Animal với các phương thức makeSound(), move(), và classify().  `
    interface Animal
    {
        public function makeSound();
        public function move();
        public function classify();
    }
    
    // Tính đa hình:
    // Các lớp Snake và Chicken triển khai interface Animal,
    // cho phép các phương thức trong interface này có thể được gọi trên bất kỳ đối tượng nào của các lớp này.
    class Snake implements Animal
    {
        public string $special;
    
        public function makeSound(): string
        {
            return 'sisisis';
        }
    
        public function move(): string
        {
            return 'RUN';
        }
    
        public function classify(): string
        {
            return 'zoo';
        }
        
    }
    
    class Chicken implements Animal
    {
        public string $name;
    
        public function makeSound(): string
        {
            return 'chick chekc!';
        }
    
        public function move(): string
        {
            return 'chickern run';
        }
    
        public function classify()
        {
            return 'farm';
        }
    }
    
    // Tính trừu tượng (Abstraction):
    interface ClassifyAnimal
    {
        public function displayAnimalWithClassify();
        public function addAllAnimal(Animal $animal);
    }
    
    // Tính đa hình:
    class AnimalCollection implements ClassifyAnimal
    {
        private array $animals = [];
        private string $classification;
    
        public function __construct(string $classification)
        {
            $this->classification = $classification;
        }
    
        public function addAllAnimal(Animal $animal): void
        {
            $this->animals[] = $animal;
        }
    
        public function displayAnimalWithClassify(): void
        {
            foreach ($this->animals as $animal) {
                if ($animal->classify() === $this->classification) {
                    $name = strtolower(get_class($animal));
                    echo "
                        Name: $name
                        Sound: {$animal->makeSound()}
                        Move: {$animal->move()}
                    ";
                }
            }
        }
    }
    
    // tao doi moi
    $animal1 = new Snake();
    $animal1->special = 'TRUON';
    
    // tao doi tuong moi
    $animal2 = new Chicken();
    $animal2->name = 'chieck black';
    
    // them tat ca vao vuon thu va phan loai
    $zoo = new AnimalCollection('zoo');
    $zoo->addAllAnimal($animal1);
    $zoo->addAllAnimal($animal2);
    
    $zoo->displayAnimalWithClassify();
    
    // them tat ca vao farm va phan loai
    $farm = new AnimalCollection('farm');
    $farm->addAllAnimal($animal1);
    $farm->addAllAnimal($animal2);
    
    $farm->displayAnimalWithClassify();

## Kết luận
Cho dù là những bài học cơ bản hay là nâng cao. Hiểu được những nguyên tắc cơ bản trước giúp chúng ta có thể theo đuổi đam mê của mình.

Và mình là diepchiaser. Xin cảm ơn các bạn!

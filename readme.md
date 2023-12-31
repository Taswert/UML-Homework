    Описание предметной области:
        Ресторан в котором:
            - Владелец набирает на работу сотрудников (повара, официанты, охранники) или уволняет их
            - Повара готовят еду
            - Официанты приносят еду клиентам
            - Охранники следят за безопасностью ресторана и могут выпроводить клиента
            - Клиенты оставляют заказы и употребляют еду
            - доставщики (если сущностей не хватит)
        
    Анализ сущностей предметной области:
        1. Владелец
            Атрибуты:
            - name: str // Имя владельца
            - age: int // Возраст владельца
            Методы:
            + fire(name: str) // увольнение работника
            + hire(name: str, jobType int) // Найм сотрудника на определённую работу
            + giveSalary(name: str) // Выдача зарплаты
            + changeSalary(jobType: int, newSalary: int) // Смена зарплаты определённому типу работы
    
        2. Работник
            Атрибуты:
            - name: str // Имя сотрудника
            - age: int // Возраст сотрудника
            - workExperience: float // Стаж работы в годах
            - salary: int // Зарплата сотрудника
            - jobType: int // Место работы сотрудника (официант, повар или охранник)
            Методы:
            + quitJob() // Увольнение с работы
            + getName(): str // Получение имени работника
    
        3. Повар
            Атрибуты:
            - cookedAmount: int // Количество приготовленной еды
            Методы:
            + cook(foodType: int) // Приготовить определённое блюдо
    
        4. Официант
            Атрибуты:
            - deliveredAmount: int // Количество доставленной еды
            Методы:
            + deliverFood(name: int, foodType: int) // Доставить определенное блюдо определённому клиенту
    
        5. Охранник
            Атрибуты:
            - escortedOutAmount: int // Количество выпровожденных клиентов
            Методы:
            + escortOut(name: int) // Выпроводить определённого клиента
    
        6. Клиент
            Атрибуты:
            - name:str // Имя клиента
            - age:int // Возраст клиента
            - isEscortedOut: boolean // Был ли выпровожден данный клиент
            Методы:
            + eat() // Съесть своё блюдо
            + getName(): str // Получение имени клиента
    
        7. Еда
            Атрибуты:
            - foodType: int // Вид блюда
            - isCooked: boolean // Приготовлено ли блюдо
            - isDelivered: boolean // Доставлено ли блюдо
    
        8. Ресторан
            Атрибуты:
            - name: str // Название ресторана
            - workers: List<Работник> // Список работников

# Задача 1

Опишите кратко, в чём основное отличие полной (аппаратной) виртуализации, паравиртуализации и виртуализации на основе ОС.
# Ответ
    Полная  виртуализация полностью эмулирует физический компьютер с соответствующими физическими устройствами. Изолированная ОС.

    Паравиртуализация использует гостевые ОС для работы с гипервизором. Прямое использование гостевой ОС аппаратных ресурсов хоста.

    Виртуализация на уровне ОС, виртуализирует пользовательское окружение ОС и позволяет запускать изолированные контейнеры на одной ОС.

В чём разница при работе с ядром гостевой ОС для полной и паравиртуализации?
Разница во взаимодействии с гипервизором. В полной виртуализации гостевая ОС работает в изолированной виртуальной машине (ВМ), которая полностью эмулирует физическое аппаратное обеспечение, в паравиртуализации гостева ос взаимодействует с гипервизором и знает о его наличии и работает с аппаратным обеспечением через отдельные драйверы и программные вызовы.


# Задача 2

Выберите один из вариантов использования организации физических серверов в зависимости от условий использования.

Организация серверов:

    физические сервера,
    паравиртуализация,
    виртуализация уровня ОС.

Условия использования:

    высоконагруженная база данных, чувствительная к отказу;
    различные web-приложения;
    Windows-системы для использования бухгалтерским отделом;
    системы, выполняющие высокопроизводительные расчёты на GPU.

Опишите, почему вы выбрали к каждому целевому использованию такую организацию.
# Ответ: 
1. Высоконагруженная база данных, чувствительная к отказу. Физические сервера. Физические серверы обеспечат полный доступ к аппаратным ресурсам, исключив возможность конфликтов с другими виртуальными машинами.
Это обеспечит предсказуемость производительности и повышенную стабильность работы базы данных.
2.Различные web-приложения. Виртуализация уровня ОС (контейнеризация).Виртуализация уровня ОС, такая как контейнеризация (например, Docker),
позволяет запускать каждое приложение в изолированной среде с общим ядром ОС, что обеспечивает высокую плотность размещения и легкость масштабирования.
3. Windows-системы для использования бухгалтерским отделом. Физические сервераЭто обеспечит изоляцию и предотвращение возможных утечек данных между виртуальными машинами.
Кроме того, с физическими серверами легче управлять и обеспечивать дополнительные уровни безопасности.
4. Системы, выполняющие высокопроизводительные расчеты на GPU. Паравиртуализация. Паравиртуализация позволяет использовать прямой доступ к аппаратным ресурсам, что делает её наиболее подходящим вариантом для выполнения высокопроизводительных расчетов на GPU.
5. Это обеспечит максимальную производительность, так как виртуальные машины смогут непосредственно управлять GPU и получать высокую производительность вычислений.

# Задача 3

Выберите подходящую систему управления виртуализацией для предложенного сценария. Детально опишите ваш выбор.

Сценарии:

  1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
  2. Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
  3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
  4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.
# Ответ
1. ESXi, Hyper-V идеальное решение для машин данного типа. Централизованное управление, балансировка нагрузки, репликация данных.
2. Xen, Proxmox
3. Hyper-V
4. VirtualBox

# Задача 4

Опишите возможные проблемы и недостатки гетерогенной среды виртуализации
(использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем.
Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет? Мотивируйте ваш ответ примерами.
# Ответ
1. Управление. Отстутствие централизованной системы управления, разные среды и наборы инструментов.
2. Возможноые ограничения по интеграции между средами.
3. Разные системные требования, что влечет просадки по производительности.

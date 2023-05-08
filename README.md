 # 4IFIR 1.5

[ENGLISH GUIDE](README_ENG.md)

**Автор проекта @Cooler3D**

[Группа в телеграме](https://t.me/kefir_switch/48074)

![](https://gbatemp.net/attachments/1_done-png.359267/)

**ВНИМАНИЕ! Над инструкцией все еще ведется работа! Пулреквесты с исправлениями и дополнениями приветствуются** 

Инструкция обширная. Используйте поиск для того, чтобы успешно ей пользоваться. 

Сборник модифицированных компонентов, призванный максимально упростить разгон Nintendo Switch, а также улучшить пользовательский опыт за счет дополнительного функционала.
Модификация предназначена для тех, кто хотел бы выжать максимум из своей консоли, добиться графики уровня PS4 (рекомендуется использовать в связке с [модами ув. ECLIPSE00074](https://4pda.to/forum/index.php?showuser=176532)), разблокировать 60fps, ускорить загрузки, зафиксировать нативное разрешение, эмулировать PS2 в fullspeed-е (при наличии эмулятора для Switch, разумеется), снизить шум системы охлаждения и т.д. 

В случае с 4IFIR, под разгоном подразумевается не разблокировка частот в пределах штатных таблиц, а именно что разгон, включающий overvolting каждого разгоняемого компонента. Устанавливая модификацию без теоретической подготовки, вы снимаете с автора ответственность за любые возможные последствия, включая выход консоли из строя, и полностью берете риски на себя. По моим схемотехническим расчетам, если они верны, проблем возникнуть не должно. В настоящий момент прецедентов выхода из строя: 0. Тем не менее, ваша консоль может стать первой, абсолютно безопасным разгон быть не может по определению, я вас предупредил. От потенциальных программных проблем вас застрахует использование EmuNand, FAT32 и наличие бекапов. Во-избежание конфликтов, рекомендуется проводить установку начисто.

## Содержание 

1. [Что может 4IFIR](#что-может-4ifir)
1. [Состав 4IFIR](#состав-4ifir)
1. [Установка](#установка)
   * [Установка с нуля (она же переустановка начисто)](#установка-с-нуля-она-же-переустановка-начисто)
   * [Установка (с кефира или другой сборки)](#установка-с-кефира-или-другой-сборки)
   * [Обновление (переход с предыдущих версий)](#обновление-переход-с-предыдущих-версий)
1. [Как использовать 4IFIR](#как-использовать-4ifir)
   * [Включение и отключение модулей](#включение-и-отключение-модулей)
   * [Управление режимом работы консоли (портатив \ докстанция, ReverseNX-RT)](#управление-режимом-работы-консоли-портатив--докстанция-reversenx-rt)
   * [Разгон](#разгон)
      * [Настройки частот и говернор (governor) (4IFIR Kraken)](#настройки-частот-и-говернор-governor-4ifir-kraken)
      * [STAGE (Self-Torture by Aggressive Generation of Explosions)](#stage-self-torture-by-aggressive-generation-of-explosions)
   * [Выжимаем больше - читы и патчи на улучшение графики](#выжимаем-больше---читы-и-патчи-на-улучшение-графики)
      * [Читы](#читы)
      * [Модификации](#модификации)
      * [FPSLocker](#fpslocker)
   * [Оптимизация работы, выбор подходящих частот и энергопотребление](#оптимизация-работы-выбор-подходящих-частот-и-энергопотребление)
1. [Проблемы и их решения](#проблемы-и-их-решения)
   * [Проблемы с батареей](#проблемы-с-батареей)
      * [Батарея начала разряжаться до 1% со 100% за считаные минуты, однако без проблем работает на 1% несколько часов](#батарея-начала-разряжаться-до-1-со-100-за-считаные-минуты-однако-без-проблем-работает-на-1-несколько-часов)
      * [При игре с включенным разгоном через некоторое время показывается значок пустой батареи](#при-игре-с-включенным-разгоном-через-некоторое-время-показывается-значок-пустой-батареи)
      * [Игра перестала запускаться и стала вылетать](#игра-перестала-запускаться-и-стала-вылетать)
      * [Ведьмак 3 не запускается](#ведьмак-3-не-запускается)
      * [FPS в игре всегда показывает 0\254 \ ReverseNX не переключает режимы](#fps-в-игре-всегда-показывает-0254--reversenx-не-переключает-режимы)
1. [FAQ](#faq)
1. [Лицензии](#лицензии)
1. [Благодарности](#благодарности)

## Что может 4IFIR

* Разгон вплоть до значений в 2397 Mhz для CPU, 1536 Mhz для GPU, 24хх Mhz для RAM (точный потолок значения индивидуален для каждой консоли)
* Автоматический овервольтинг
* Автоматический буст при загрузке игры 
* Поддержка говернора - снижения потребления ресурсов когда они не требуются консоли 
* Видеозапись без ограничений во всех играх, кроме нескольких не поддерживаемых
* Беспроводная видеотрансляция с повышенным битрейтом, 60 кадрами в секунду, на внешние мониторы - практически без задержек
* Эмуляция док режима
* Ускоренная зарядка
* Снижение порога тока для Official Charger
* Радикальное снижение шума системы охлаждения
* Overlay c FPS и системными метриками
* Над-экранное меню, для управления перечисленными возможностями на лету
* Фоновый FTP сервер
* Необходимые для совместной работы всего перечисленного системные модули

## Состав 4IFIR

1. **[4efirosphere](https://cloud.sintez.io/s/4IFIR?path=%2FMariko)**, форк [Atmosphere](https://github.com/Atmosphere-NX/Atmosphere), раскрывающий разгонный потенциал консоли
1. **[Сигпатчи](https://jits.cc/patches)**, раскрывающие игровой потенциал консоли
1. **[4ekate](https://cloud.sintez.io/s/4IFIR)**, форк [hekate](https://github.com/CTCaer/hekate), раскрывающий потенциал разгона памяти консоли
1. **Установленные пейлоады**:
   * [Lockpick_RCM](https://github.com/shchmue/Lockpick_RCM) - программа для дампинга ключей консоли
   * [TegraExplorer](https://github.com/rashevskyv/TegraExplorer/) - низкоуровневый файловый менеджер для работы с системой 
1. **Установленное Homebrew**
   * [AiO Switch Updater](https://github.com/rashevskyv/kefir-updater) - программа для обновления 4IFIR до актуальной версии 
   * [Homebrew App Store 2.2](https://github.com/fortheusers/hb-appstore/releases) - магазин приложений
   * [Daybreak](https://github.com/Atmosphere-NX/Atmosphere/tree/0.14.1/troposphere/daybreak) - программа для обновления системного ПО
   * [DBI](https://github.com/rashevskyv/dbi) - потенциально лучший файловый менеджер, менеджер сохранений и установщик программ на консоль
   * [Fizeau](https://github.com/averne/Fizeau) - программа, позволяющая менять параметры отображения цветов на экране
   * [SysDVR](https://cloud.sintez.io/s/4IFIR), форк [SysDVR](https://github.com/exelix11/SysDVR) - программа для беспроводной передачи изображения с консоли на ПК или другие устройства
   * [sys-ftpd](https://cloud.sintez.io/s/4IFIR), форк [sys-ftpd](https://github.com/cathery/sys-ftpd) - FTP сервер, работающий в фоне
1. **Установленные модули**. Модули - это дополнительные компоненты, работающие внутри Atmosphere и позволяющие делать разные крутые штуки, как-то использование xbox-сoвместимых контроллеров, эмуляцию amiibo, разгон и прочее
   * [SaltyNX](https://cloud.sintez.io/s/4IFIR), форк [SaltyNX](https://github.com/masagrator/SaltyNX), фоновый модуль, позволяющий модифицировать файлы\процессы в консоли, поддерживает плагины. Не совместим в 32-х битными играми (список на гитхабе проекта). Требуется для работы некоторых других модулей (например, ReverseNX)
   * [ReverseNX-Tool](https://cloud.sintez.io/s/4IFIR), форк [ReverseNX-Tool](https://github.com/masagrator/ReverseNX-Tool) - программа, которая принудительно меняет режимы работы консоли на докстанцию и портатив, вне зависимости от того  находится консоль в доке или нет. Потенциально улучшает картинку в портативе за счет того, что рендерит изображение так, как будто консоль в докстанции. 
   * [sys-clk](https://cloud.sintez.io/s/4IFIR), форк [sys-clk](https://github.com/retronx-team/sys-clk), модуль отвечающий за разгон процессора, памяти, GPU, что приводит к лучшей производительности
   * [sys-con](https://github.com/cathery/sys-con) - модуль, позволяющий подключать к консоли по USB практически любые геймпады
   * [Tesla Overlay Menu](https://cloud.sintez.io/s/4IFIR), форк [Tesla Overlay Menu](https://github.com/WerWolv/Tesla-Menu/) - специальное оверлей-меню для взаимодействия с системой: разгон, управление режимами через ReverseNX, включение читов, прочее. 
     - [FPSLocker](https://github.com/masagrator/FPSLocker) - оверлей, позволяющий заблокировать FPS в играх 
     - [nx-ovlloader](https://github.com/WerWolv/nx-ovlloader/) - с помощью этого модуля осуществляется переключение установленных модулей через Tesla 
     - [ovlEdiZon](https://github.com/proferabg/EdiZon-Overlay/releases) - оверлей для использования читов
     - [ovlSysmodules](https://github.com/WerWolv/ovl-sysmodules/) - оверлей для включения и отключения установленных системных модулей
     - [InfoNX-ovl](https://github.com/renA21/InfoNX/) - оверлей, показывающий информацию о батарее/CPU/GPU/DRAM(EMC)
     - [QuickNTP](https://github.com/nedex/QuickNTP) - оверлей для синхронизации часов через интернет, поскольку родная в чифире отключена 
     - [Status-Monitor-PRO](https://cloud.sintez.io/s/4IFIR), форк [Status-Monitor-Overlay](https://github.com/masagrator/Status-Monitor-Overlay) - модуль для контроля параметров консоли в реальном времени. Может выступать в качестве  счетчика FPS в левом верхнем углу экрана
     - [sys-ftpd-ovl](https://github.com/SegFault42/sys-ftpd-ovl) - оверлей для работы с sys-ftpd через Tesla 
     - [sysdvr-overlay](https://github.com/Hartie95/sysdvr-overlay), форк [sysdvr-overlay](https://github.com/Hartie95/sysdvr-overlay) - оверлей для настройки SysDVR через Tesla 
     - sys-clk overlay - оверлей для управления разгоном через Tesla 
     - Fizeau overlay  - оверлей для настройки Fizeau через Tesla 
     - ReverseNX-RT overlay - оверлей для переключения режима работы консоли через Tesla 

## Установка 

**ВАЖНО! Строго следуйте инструкции и не откланяйтесь от нее. В случае возникновения проблем, вернитесь к инструкции и переустановите чифир начисто.**

Версирование чифира очень условное (проще сказать, отсутствует вообще), поэтому множество обновлений может выходить при этом не меняя версии чифира вообще. Следить за новыми версиями можно в [чате чифира](https://t.me/kefir_switch/48074), или на [этой странице](https://github.com/rashevskyv/4ifir-checker), где будет показано когда вышла новая версия и что конкретно в ней изменилось. [Обновление же производится через AIO](#обновление-переход-с-предыдущих-версий).

### Установка с нуля (она же переустановка начисто)
1. Удалите с карты памяти всё, кроме папки Nintendo и emummc (если есть) (Папку с бекапами сохранений, например JKSV, тоже не стоит удалять)
   * Карта должна быть в [FAT32](https://format.customfw.xyz)
   * Работать с картой памяти рекомендуется через картридер, не через консоль.
2. Распакуйте [4IFIR](https://sintez.io/4IFIR.zip) на карту памяти консоли
3. Вставить карту в консоль и включить

### Установка (с кефира или другой сборки)
Сделайте [чистую установку](#установка-с-нуля-она-же-переустановка-начисто)

### Обновление (переход с предыдущих версий)
1. Запустите [**Homebrew Launcher**](https://switch.customfw.xyz/hbl) > **All in One Updater**
   * Если вместо запуска приложения вы получаете черный экран, перекачайте приложение вручную из его [репозитория](https://github.com/HamletDuFromage/aio-switch-updater) и вручную пропишите в Custom downloads > Add custom link этот адрес `https://sintez.io/aio.zip`, после чего перезапустите приложение
1. Перейдите в **Custom Downloads** > **4IFIR 1.5** > **Continue**, на запрос о перезаписи `ini`, выберите **Yes**, на запрос о переустановке hekate выберите **No**, консоль перезагрузится

2. Перезагрузите консоль

## Как использовать 4IFIR 

Все настройки осуществляются через Tesla-меню, которое вызывается сочетанием клавиш (L)+(R3)+(▼), где (L) - верхний бампер левого джойкона, (R3) - нажатие на правый стик, а (▼) - кнопка вниз на "крестовине". 
После одновременного нажатия этих трех кнопок появится Tesla-menu со следующими пунктами: 

* **FPSLocker** - модуль для блокировки частоты кадров в играх
* **Fizeau** - модуль для управлением дисплея и его цветовыми профилями
* **InfoNX** - модуль, показывающий расширенную информацию о потреблении энергии консолью
* **QuickNTP** - модуль, позволяющий синхронизировать часы через интернет, поскольку встроенный метод синхронизации в кефире отключен 
* **ReverseNX-RT** - модуль, позволяющий принудительно выбрать режим работы консоли (портативный или докстаниця)
* **Status Monitor** - модуль, показывающий метрики работы системы в реальном времени поверх экрана, не отбирая управление у игры. Есть много режимов работы, в том числе режим, позволяющий вывести счетчики частот и FPS в левом верхнем углу экрана
* **EdiZone** - модуль для управления читами 
* **Sysmodules** - модуль, для управления модулями. Позволяет включать\отключать установленные модули
* **4IFIR Kraken** - модуль для управления профилями разгона
* **SysDVR Overlay** - модуль, управляющий потоковой передачей изображения с консоли на ПК по WiFi или кабелю 

Нажав **(A)** на пункте, вы откроете его персональное меню.

### Включение и отключение модулей 

Модуль **Sysmodules** позволяет включать и выключать выбранные модули, а так же управлять их автозагрузкой. Имейте ввиду, что некоторые модули можно включать и выключать без перезагрузки, однако ряд модулей после включения требуют перезагрузки консоли. 

Справа от названия модуля указано его состояние, например **On | х**, где On говорит о текущем состоянии модуля (On - включен, Off - выключен), а **х** о том стоит ли модуль в автозагрузке (**х** - не стоит, **иконка домика** - стоит). 

Кнопкой **(A)** можно включить или выключить модуль. Кнопка (Y) включает или выключает автозагрузку модуля. Если при нажатии на кнопку (A) модуль не меняет своё состояние, значит им можно управлять только перезапуском консоли. Включите автозагрузку модуля и перезагрузите консоль, чтобы он начал работать, или выключите и перезагрузите, чтобы перестал. 

Модули, которые можно включать в любой момент сгруппированы сверху в группу **Dynamic**, а те, что требуют перезагрузки в группу **Static**.

### Управление режимом работы консоли (портатив \ докстанция, ReverseNX-RT)

Модуль **ReverseNX-RT** позволяет принудительно включать режим докстанции при игре в портативе и наоборот. С помощью кнопки **Change system control** нужно включить принудительное управление сменой режимов (отображается в строке **Controlled by system**, положение **No** означает, что можно менять режимы вручную). После чего можно переключать режимы кнопкой Change mode (отображается в строке **Mode**, где **Docked** - режим докстанции, **Handheld** - портатив).

Важно понимать, что в режиме докстанции консоль принудительно повышает частоты работы процессора, в следствии чего картинка становится более качественной, но и быстрее расходуется батарея.

### Разгон 

В чифире разгон достигается глубокими оптимизациями компонентов HOS. Эффективность работ железа в пересчете на ватт, примерно в 3-5 раз выше, чем в стоковых частотах без разгона. Все это благодаря прорывной оптимизации памяти (преодоление порога частоты и таймингов). В данный момент в 4IFIR не реализовано андервольтинга в классическом его понимании, однако, благодаря оптимизациям чифир гараздо экономнее расходует энергию при разгоне, нежели его конкуренты. 

Для стабильного разгона вам необходимо подобрать стейдж на котором ваша консоль способна работать, а затем частоты работы CPU\GPU\Памяти и другие настройки. Все это делается экспериментальным путём и индивидуально для каждой конкретной пристави и, более того, для каждой конкретной игры.

#### Настройки частот и говернор (governor) (4IFIR Kraken)

Настройка разгона осуществляется через модуль 4IFIR Kraken overlay.

В заголовке располагаются следующие параметры: 
* **App ID** - показывает titleid запущенной игры 
* **Profile** - параметр синхронизирован с настройками ReverseNX-RT (если включена соответствующая настройка в параметрах) и показывает в каком режиме сейчас работает консоль (**Docked** - режим докстанции, **Handheld** - портатив)
* **CPU** - текущая частота процессора 
* **GPU** - текущая частота ядра видеопроцессора 
* **MEM** - текущая частота памяти 
* **SOC** - температура процессора (SoC - система на чипе, означает, что на одном чипе находится и видеоядро и центральный процессор, потому температура у них одна на двоих)
* **PCB** - температура платы консоли 
* **Skin** - температура самой консоли (?)

* **Enable** - отвечает за активацию разгона. On - включен, Off - отключен 
* **Edit app Profile** - настройка профиля разгона для запущенного приложения. Указанные настройки будут автоматически применяться при запуске приложения. Имеют средний приоритет. 

* Advanced
   * **Temporary overrides** - настройки разгона для всех приложений. Указанные настройки применяются для всех запускаемых приложений и действуют до перезагрузки приставки. Имеют наивысший приоритет.
   * **Global profile** - настройки разгона для всех приложений. Указанные настройки применяются для всех запускаемых приложений. Имеют самый низкий приоритет. 
   * **Miscellaneous** - дополнительные настройки консоли, например, ограничение вольтажа зарядки, автобуст, ограничение процента зарядки и другие. Подробнее будет рассмотрено отдельно. 

Разгон осуществляется с помощью смены максимальной частоты для CPU/GPU/Памяти через настройки разгона **Global profile**/**Edit app Profile**/**Temporary overrides**. Причем настройки будут применяться в зависимости от приоритета (**Temporary overrides** -> **Edit app Profile** -> **Global profile**). Наивысший приоритет у **Temporary overrides**, если там не указано никаких настроек, то программа смотрит в настройки из **Edit app Profile**, если там пусто, то применяются настройки из **Global profile**. И если уже там ничего нет, то ставятся настройки системы по-умолчанию (**Default**).

**Global profile** и **Edit app Profile** содержат разделение на профили: 
  * **Docked**
  * **Handheld**
  * **Charging**
  * **Official Charging**
  * **USB Charger** 

Профили имеют так же свой приоритет. От наивысшего к низшему: **Docked** -> **Official Charging** / **USB Charger** -> **Charging** -> **Handheld**. Принцип применения ровно такой же. Режим **Docked** имеет наивысший приоритет и перезаписывает значения профилей с приоритетом ниже. **Official Charging** или **USB Charger** имеют одинаковый приоритет и перезаписывают значения профилей **Charging** и **Handheld**, и так далее.

Профили **Docked** и **Handheld** синхронизированы с настройками Reverse-NX (можно отключить в **Miscellaneous** модуля **4IFIR Kraken**) и зависят от режима работы консоли (док/портатив). Профиль **Charging** включается при подключении любой зарядки к консоли. Профиль **Official Charger** включается при подключении оригинальной зарядки, или любой другой, но с поддержкой протокола Power Delivery. Профиль **USB Charger**, при подключении любой другой зарядки. То есть, вы можете настроить отдельный профиль разгона для зарядки от любого источника и отдельно для мощного или маломощного, причем последние имеют приоритет выше. 

**Edit app Profile** содержит в себе управление говернорами

Говернор (англ. governor) в контексте управления частотами процессора - это программа или механизм, который контролирует частоту работы процессора и его потребление энергии.

Суть работы говернора заключается в том, чтобы определить оптимальную частоту работы процессора в зависимости от нагрузки на него. Если процессор не нагружен, говернор может снизить его частоту, чтобы снизить потребление энергии и уменьшить тепловыделение. Если же процессор получает высокую нагрузку, говернор может увеличить его частоту, чтобы обеспечить высокую производительность.

* **CPU Freq Governor** - включить или выключить управление частотой **центрального** процессора
* **GPU Freq Governor** - включить или выключить управление частотой **графического** процессора

Оба эти пункта будут доступны только если в **Miscellaneous** активировано значение **Frequency Governor (Experimental)**

Включение говернора GPU в ряде игр может привести к подтормаживанию или снижению FPS (например, Metroid Prime Remastered иногда сбрасывает FPS до 30 при выходе из карты в игру). Если в вашей игре наблюдается такое, отключите говернор для GPU.

Каждый из профилей содержат в себе отдельные пункты для разгона **CPU**, **GPU** и **Memory**. Что за что отвечает легко понять по названию. В каждом из этих пунктов есть значение **Default**, которое отвечает за значение по-умолчанию, которое берется из предыдущей по приоритету настройки разгона (Temporary/App/Global/Системное значение) из профиля, соответствующего приоритета. Рабочие частоты подбираются индивидуально для каждой конкретной игры на каждой конкретной консоли. Подробнее про подбор частот будет ниже. 

* **Miscellaneous** - раздел с дополнительными настройками. Содержит в себе следующие опции:
   * **Auto CPU Boost** - активный слой автобуста. Повышает частоту CPU при нагрузке на системное ядро, что обычно означает подгрузку данных, стриминг текстур, локаций и т. п. На Erista лучше отключать, поскольку влияет на время работы от батареи
   * **Sync ReverseNX Mode** - настройка, синхронизирующая состояние значения ReverseNX с профилем sys-clk. То есть, если в реверсе стоит **Handheld**, то активный профиль в sys-clk будет **Handheld**, если **Docked**, то **Docked** соответственно
   * **Frequency Governor (Experimental)** - включает говерноры в **Edit app Profile**
   * **Charging current** - ограничение тока зарядки
   * **Charging Limit** - ограничение до которого приставка будет заряжаться
   * **Force Disable Charging** - опция, позволяющая не заряжать батарею при работе от зарядки. То есть, батарея не будет садиться, но и фактически не будет заряжаться тоже. Позволяет избежать проблем с десинхронизацией батареи 
   * **Screen Backlight** - отключает подсветку экрана. Полезно в связке с sys-dvr 
   * **Info** - различные метрики: 
      * **Charger** - тип зарядного устройства, подключенного к консоли. Показывается вольтаж и ампераж, а так же мощность в Ваттах
      * **Battery** - напряжение на батарее и её температура
      * **Current Limit** - 
      * **Charging Limit** - значение, указанное в **Charging current**
      * **Raw Charge** - Заряд батареи, который отдает контроллер зарядки 
      * **Battery Age** - "здоровье" батареи
      * **Power Role** - 
      * **Current Flow** - текущее потребление 
      * **CPU Volt** - вольтаж CPU 
      * **GPU Volt** - вольтаж GPU 
      * **DRAM Volt** - вольтажи памяти

#### STAGE (Self-Torture by Aggressive Generation of Explosions)

Чем выше STAGE, тем агрессивнее оптимизация таймингов/значений андервольтинга. Тем быстрее и энергоэффективнее игровая консоль. Стоковый 4IFIR 1.5 должен работать на любой консоли и его производительность эквивалентна STAGE 6+. Вероятность того, что у Вас заработают ST7 и выше, зависит от [удачности процессорного бининга](https://www.computerra.ru/285384/dzhekpot-kremnievoj-loterei-chto-takoe-binning-protsessory/) конкретно вашей консоли.

Выбор стейджей осуществляется в **AiO Updater**, в меню **Custom Downloads**. После выбора стейджа консоль необходимо перезагрузить.

Для выбора стабильного стейджа нужно тестировать консоль следующим образом:

**ВНИМАНИЕ!!!** Если на каком-либо из этапов при тестировании стейджа произошло зависание, либо игра зависла, либо на экране появились артефакты, либо проявилось какое-либо неожиданное поведение консоли, понижайте стейдж. Текущий ваша консоль не тянет!

1. Выберите максимальный из доступных стейджей в AiO, перезагрузитесь 
1. Отключите говерноры (**4IFIR Kraken** > **Frequency Governor (Experimental)** > **Off**)
1. Выберите максимально доступную частоту памяти.
1. Если консоль не зависла, выберите максимально доступную частоту GPU
1. Если консоль не зависла, выберите максимально доступную частоту CPU
1. Если консоль не зависла, запустите любую тяжелую игру и протестируйте с ней минут 10-15. 
1. Если никаких глюков/глитчей/зависаний/артефактов не обнаружено, поздравляем, ваша консоль выиграла в кремниевой лотерее.

Вы можете добиться стабильной работы стейджа понизив частоты памяти или GPU. 

### Выжимаем больше - читы и патчи на улучшение графики 

#### Читы 

Помимо возможности включить режим докстанции при игре в портативе, можно дополнительно установить графические модификации для игр. Некоторые из них активируют большую частоту кадров, некоторые позволяют использовать производительность разогнанной консоли для улучшения отображаемой картинки, некоторые наоборот, улучшают производительность игры для стабильной работы на частотах без разгона. 

Читы для разблокировки 60FPS в некоторых играх можно взять в **AiO Updater** > **Download cheats** > **Download graphics enhancing cheats**. Если для установленных игр есть соответствующие читы, то они будут установлены автоматически. Помните что если для этих игр у вас уже были установлены читы, то установка читов для разблокировки удалит уже имеющиеся читы. Однако, если у вас есть читы для разблокировки FPS, то установка обычных читов через апдейтер просто добавит их, при этом сохранив читы на разблокировку. 

Активация читов проводится через меню **Tesla** > **EdiZon** > **Cheats** во включенной игре. В появившемся меню активируйте необходимый чит. После перезапуска игры, читы, что вы активировали ранее так же будут активны!

#### Модификации 

Моды для улучшения картинки нужно искать [на 4PDA](https://4pda.to/forum/index.php?act=findpost&pid=81825647&anchor=Spoil-81825647-8) или в телеграм-боте [Switch_library_bot](https://t.me/Switch_library_bot) по запросу `/mods` (пароль для бота - `kefir`).

Установка мода различается в зависимости от того как именно он сделан. 

* Если мод идет ввиду LayeredFS папки, то его нужно класть в `/atmosphere/contents/%TitleID%/romfs`, где TitleID - title id вашей игры, состоящий из 16 символов в 16-тиричной системе исчисления (например, 01002CC003FE6000). Отнеситесь внимательно к тому как именно такая модификация распространяется и не допустите вложенности папок. Например, если вы видите что в архиве с модом папка `atmosphere`, то просто распакуйте ее в корень карты памяти и согласитесь на замену файлов. Если в архиве лежит папка с title id игры, поместите ее в папку `/atmosphere/contents/`. Убедитесь, что папка не дублируется (например `/atmosphere/contents/01002CC003FE6000/romfs` - правильно, а `/atmosphere/contents/01002CC003FE6000/01002CC003FE6000/romfs` или `/atmosphere/atmosphere/contents/01002CC003FE6000/romfs` - не правильно), иначе мод не будет работать. 
* Если мод идёт в виде IPS-патча, то есть в виде файла или файлов с расширением `*.ips`, то поместите его в папку `atmosphere/exefs_patches`. В папке `atmosphere/exefs_patches` можете создать папку с названием мода, это допускается. Если в архиве с модом есть просто папка `exefs_patches`, то поместите её с заменой в папку `atmosphere`. Часто моды могут комбинировать оба способа, тогда нужно понять что именно и куда копировать. Если вам что-то не понятно, попробуйте поискать информацию там, где вы эти моды качали или в текстовом файле, который может распространяться вместо с модом. 

Модификации установленные таким образом автоматически активируются при запуске игры. 

Помните, что важна версия игры для которой делалась модификация. Мод, сделанный для одной версии игры может не заработать на другой. 

Не стесняйтесь играть с частотами и использовать Status Monitor для достижения наилучшего стабильного результата!

#### FPSLocker

С помощью этого плагина можно разлочить частоту кадров в некоторых играх без использования читов. 

Метрики в заголовке: 
* **Большое число справа** - показывает, сколько кадров прошло за последнюю секунду для запущенной игры. Позволяет убедиться, что программа работает верно
* **Interval Mode** - внутреннее значение игрового движка на базе NVN API, может принимать значение **0**, **1** или ****2****. Меняя это значение мы можем изменить максимальное количество FPS в игре. **2** - 30 FPS, **1** - 60 FPS, **0 - значить у игры нет ограничения на количество FPS, либо используется другое API. 
* **Custom FPS Target** - показывает максимальное количество FPS для данной игры. Если игра использует собственные ограничения FPS движка, а не стандартное, то может быть невозможно разблокировать более 30 FPS без дополнительных патчей

Переключатели:
* **Increase/Decrease FPS target** - изменить целевое количество кадров в секунду с шагом в 5 FPS. **Минимум** - 15 FPS, **максимум** - 60 FPS. Если FPS установлено более 30, то **Interval Mode** устанавливается на 1. В противном случае ставится 2.
* **Disable custom FPS target** - убирает ограничение FPS в зависимости от установленного **Interval Mode**. Если **Interval Mode** 2, то игра будет упираться в 30 FPS, если 1, то в 60. 
* **Sync Wait (!)** - это опасная настройка, которая в большинстве случаев будет приводить к падению игры (например, Witcher 3 и Breath of The Wild), но в некоторых случаях может принести пользу отключив двойную буферизацию, привнеся небольшие графические артефакты артефактов (например, Xenoblade Chronicles 3). Используйте с осторожностью. Рекомендуется держать **включенной**.
* **Save settings** - сохранить профиль для текущей запущенной игры, который будет автоматически загружен плагином при запуске в следующий раз. Не используйте эту функцию, если вы отключили синхронизацию (Ынтс Wait Off) и не проверили ее на безопасность, чтобы не пришлось вручную удалять сохраненный профиль. Профиль сохраняется в `SaltySD/plugins/FPSLocker/TITLEID.dat`

### Оптимизация работы, выбор подходящих частот и энергопотребление 

Чтобы достичь оптимальной производительности и избежать излишнего расхода энергии на вашем устройстве, нужно подобрать такие параметры частот, чтобы игра не тормозила и не более. Для этого рекомендуется использовать Status Monitor - инструмент, который позволяет отслеживать загрузку компонентов вашего устройства.

Для того, чтобы найти оптимальный баланс между производительностью и энергопотреблением, вы можете понизить (или повысить) частоты настройки в соответствии с результатами загрузки компонентов в Status Monitor. Найдите точку, где железо не загружено на 100%, но находится близко к этому уровню. Помните, что на свитче "узким горлышком" является память, при этом гонится она фактически бесплатно, то есть ее можно ставить на максимум при котором устройство работает стабильно, и это не повлияет на расход батареи. Чем выше стейдж, тем "дешевле" для консоли разгон памяти и тем он эффективнее. Гнать CPU обычно толку мало (но бывают и исключения). Поэтому, оптимальным вариантом с которого стоило бы начать, является максимальный разгон памяти и разгон CPU\GPU где-то на середину. Говерноры при этом рекомендуется отключить. Если игра при таком варианте тормозит, добавьте частоту GPU и делайте это до тех пор, пока тормоза не уйдут совсем. После этого включите говерноры. Если наблюдаются просадки FPS после их включения, отключите говернор GPU, поскольку часто именно он может приводить к просадкам. 

Не гонитесь за частотами и цифрами. Единственным мерилом удачного разгона является ваш комфорт при игре. Частоты не отражают фактической производительности, и тем более энергопотребления. Обратите внимание, что каждое устройство имеет уникальные характеристики, поэтому необходимо настраивать частоты в соответствии с конкретной моделью вашего устройства и играми, которые вы собираетесь запускать на нем. А каждая игра имеет уникальные требования. 

С помощью модуля **InfoNX** можно следить за энергопотреблением консоли. Замеряйте потребление в тестируемой игре без разгона и с разгоном, а после найдите баланс между производительностью и энергопотреблением. Не забывайте, что чем выше потребление энергии, тем быстрее сядет батарея в портативном режиме. Для работы в докстанции или от зарядки, энергопотребление не так уж и важно.

## Проблемы и их решения

### Проблемы с батареей 

Аккумулятор не деградирует от силы тока, а только при достижении определенной температуры. Однако, встроенные механизмы защиты, основанные на законах физики, разрывают цепь питания, задолго до того, как достигнутые температуры успевают навредить аккумулятору, чтобы предотвратить деградацию химических свойств ячеек.

MARIKO оснащен контроллером PMIC MAX77812 рассчитанного на токи до 6A CPU / 12A GPU. Достиг лимита = поймал маслину ушел в защиту.
ERISTA, внезапно, оснащена более мощным контроллером PMICs MAX77621 на 16A CPU / 16A GPU.

Нагрузка свыше 15 ватт (примерно; точные значения лимитов тока для разных моделей консоли указаны в спецификациях производителя) может привести к снижению оценки остаточной ёмкости аккумулятора в консоли Nintendo Switch. Контроллер питания консоли сравнивает фактические показания с показаниями, которые были вбиты с завода, и в случае превышения дергает аварийное отключение. Консоль может считать, что аккумулятор не вывез, и снижает оценку его остаточной ёмкости, на 1% при каждом сбое. Это может привести к тому, что индикатор заряда консоли начинает мгновенно опускаться до 1% заряда, когда дается нагрузка на аккумулятор. Battery Fix, может позволить "регенерировать" списанную по ошибке ёмкость аккумулятора.

#### Батарея начала разряжаться до 1% со 100% за считаные минуты, однако без проблем работает на 1% несколько часов 

Контроллер питания рассчитан на пиковое потребление энергии примерно в 15W, если оно будет превышено, то консоль аварийно активирует защиту и выключится. Вам нужно снизить аппетиты, поскольку это влияет на данные калибровки контроллера. Консоль может считать, что аккумулятор не вывез, и снизить оценку его остаточной ёмкости, на 1% при каждом сбое. Это может привести к тому, что индикатор заряда консоли начинает мгновенно опускаться до 1% заряда, когда дается нагрузка на аккумулятор. Для решения этой проблемы существует [Battery Desync Fix NX](https://github.com/CTCaer/battery_desync_fix_nx). 

**ВНИМАНИЕ!!!** Не запускайте [Battery Desync Fix NX](https://github.com/CTCaer/battery_desync_fix_nx), если у вас нет проблем с батареей, иначе они появятся! Вам нужно будет делать отдельную калибровку для стока и каждого вашего эмунанда отдельно, поскольку данные о калибровке хранятся отдельно в каждом из них! 

Для сброса статистика батареи:
1. Запустите [Battery Desync Fix NX](https://github.com/CTCaer/battery_desync_fix_nx)
1. Нажмите (X), чтобы сбросить статистику
1. Нажмите (B), чтобы выйти из приложения 
1. Перезагрузите приставку в официальную прошивку
1. Дважды полностью разрядите приставку и полностью зарядите
   * Под полной разрядкой подразумевается разрядка до состояния красной батареи и выключения HOS из-за низкого разряда. При этом сама приставка остается включенной и проснется, если подключить к ней зарядку
   * Не перезагружайте приставку пока не сделаете этого
   * Если приставка засыпает из-за низкого заряда, будите её, пока не увидите красный значок батареи
   * Если приставка выключилась из-за низкой батареи (перестает просыпаться от нажатия на кнопку питания), подключите к ней зарядник. Если приставка после этого висит на черном экране со значком батареи, отключите\подключите зарядку. Делайте так, пока не сможете снова зайти в прошивку и уже в ней заряжайте приставку до 100%, после чего повторите цикл разрядка\зарядка еще раз
   * Не оставляйте приставку заряжаться в черном экране со значком батареи, иначе прошивка восстановит прежние значения калибровки батареи, что нам не нужно, и придется начинать все с начала
1. После того как вы откалибровали батарею в сиснанде, проделайте все в точности так для каждого из эмунандов, если у вас их больше одного. 
   * Не переключайтесь между сиснандом и эмунандами пока не закончите два цикла зарядки\разрядки, поскольку прошивка восстановит прежние значения калибровки батареи, что нам не нужно, и придется начинать все с начала

#### При игре с включенным разгоном через некоторое время показывается значок пустой батареи 

Контроллер питания рассчитан на пиковое потребление энергии примерно в 15W, если оно будет превышено, то консоль аварийно активирует защиту и выключится. Это и происходит. Вероятно, вы привысили установленный в контроллере порог. Умерьте пыл и сбавьте значения частот. 

#### Игра перестала запускаться и стала вылетать 

Первым делом попробуйте удалить профиль этой игры от FPSLocker, вероятно вы отключили Sync Wait не убедившись в его безопасности. Профиль находится в `SaltySD/plugins/FPSLocker/TITLEID.dat`. Title игры можно посмотреть в **DBI** > **Browse Installed**

#### Ведьмак 3 не запускается

Удалите папку `atmosphere/exefs_patches/am` и перезагрузите приставку. Это патчи для sys-dvr, которые позволяют включить запись экрана, а как следствие и трансляцию геймплея игры, для любой игры. Удалив эти патчи, вы лишитесь этой возможности. Впрочем, если вы не собираетесь транслировать игру на ПК, то это и не важно. 

#### FPS в игре всегда показывает 0\254 \ ReverseNX не переключает режимы

Вероятна ваша игра не совместима с **SaltyNX**, который отвечает за работу эти функций. Список несовместимых игр находится [здесь](https://github.com/masagrator/SaltyNX#list-of-titles-not-compatible-with-pluginspatches)

## FAQ 

**В**: Как использование 4IFIR влияет на срок службы батареи            
**О**: Если коротко, то никак вообще. 

**В**: Моя батарея деградировала            
**О**: Она не деградировала. У нее сбилась калибровка. Вернуть заводскую емкость батареи можно по инструкции выше 

**В**: Свитч выключается при использовании разгона            
**О**: Вероятно ваш экземпляр не вывозит значения, которые вы задали. Пробуйте их понизить

**В**: Свитч разряжается до 1% со 100 за 10 минут            
**О**: Смотрите выше в разделе Проблемы и решения 

**В**: Нет говернора            
**О**: Включите **4IFIR Kraken** > **Miscellaneous** > **Frequency Governor (Experimental)**, тогда оба говернора появятся в **4IFIR Kraken** > **Edit app Profile**

**В**: Частоты прыгают            
**О**: При работе говернора так и должно быть

## Лицензии

Ниже перечислены лицензии тех программ, которые были модифицированы специально для 4IFIR. Следуя положениям этих лицензий, весь код в модификациях распространяется под той же лицензией

[GPL 2.0](https://github.com/Atmosphere-NX/Atmosphere/blob/master/LICENSE): 
  * [Atmosphere](https://github.com/Atmosphere-NX/Atmosphere)
  * [hekate](https://github.com/CTCaer/hekate)
  * [SysDVR](https://github.com/exelix11/SysDVR)
  * [sysdvr-overlay](https://github.com/Hartie95/sysdvr-overlay)
  * [Tesla Overlay Menu](https://github.com/WerWolv/Tesla-Menu/)
  * [Status-Monitor-Overlay](https://github.com/masagrator/Status-Monitor-Overlay)

[GPL 3.0](https://github.com/masagrator/ReverseNX-Tool/blob/master/LICENSE): 
  * [ReverseNX-Tool](https://github.com/masagrator/ReverseNX-Tool)
  * [sys-ftpd](https://github.com/cathery/sys-ftpd)

[THE BEER-WARE LICENSE](https://github.com/retronx-team/sys-clk/blob/develop/LICENSE): 
  * [sys-clk](https://github.com/retronx-team/sys-clk)

[MIT license](https://github.com/masagrator/FPSLocker/blob/main/LICENSE):
  * [FPSLocker](https://github.com/masagrator/FPSLocker)

No license: 
  * [SaltyNX](https://github.com/masagrator/SaltyNX)

## Благодарности 

* Atmosphere NX team
* KymPossibl
* KazushiMe
* RetroNX team
* ChanseyIsTheBest
* 4PDA

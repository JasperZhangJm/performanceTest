# performanceTest
服务端性能测试脚本

张佳民

v1-v4是调试文件，v5及以后是测试正式执行文件，测试过程中需要读取数据文件questions_v2.csv，

non-gui执行时需要创建文件夹HtmlReport，每次执行以日期加编号的方式创建目录例如2024061901，jmeter生成的html报告会放在这个目录下，如图：

<img width="257" alt="image" src="https://github.com/user-attachments/assets/9d219dfa-5ce0-4fbe-b72a-c493427c3ef8">

non-gui命令：
jmeter -n -t ./aosu_test_script/IM-GPT_V3.jmx -l ./aosu_test_script/NonUIReport/2024060601.csv -e -o ./aosu_test_script/HtmlReport/2024060601/

另一个需要创建的目录是：LocalReport，子目录是用日期和时间创建的不同的文件夹，用于存储脚本中指定存储的数据文件，这个是一个最终的结果数据文件，每个控制器生成的都是一样的，可以指定生成3中格式的数据结果文件，分别是csv、jtl、xml，如图：

<img width="257" alt="image" src="https://github.com/user-attachments/assets/578c15b7-2154-4ed1-b24f-980a1d99f0d6">

还有一个目录是：NonUIReport，这个目录是在执行non-gui时指定的目录，用于存储non-gui执行时生成的数据文件，格式可以是jtl、csv、xml任意一种，这里指定了csv格式，文件名用日期加编号命名，如图：

<img width="221" alt="image" src="https://github.com/user-attachments/assets/13fd7dc4-f1c2-4087-9e63-9d3ea5ff14f6">

LocalReport生成的数据报告如下：

<img width="1815" alt="image" src="https://github.com/user-attachments/assets/925390f0-b08e-4d5b-b4b0-36a9342bf753">

HTML报告如下：

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/22c1029c-5cd5-46a4-b5b6-ac421eaa631b">

NonUIReport生成的数据报告同LocalReport







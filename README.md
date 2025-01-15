Описание созданных программ для Практической работы 7.4. 
Каждому из заданий соответствует своя программа.

  Задание 1: необходимо создать массив из 5 целочисленных элементов, вводимых пользователем, и рассчитать среднее значение из этих элементов.
  Решение (программа Task_1).
  В программе, внутри функции main(), объявляется массив А типа int из элементов (количество которых задается переменной size=5, типа uint8_t), переменная цикла (тип uint8_t, диапазон возможных значений 0…255) и переменная Average, в которую
записывается вычисленное среднее значение. Так как полученное среднее значение может быть не целым числом, для него применен тип float. После вывода заголовка «Введите 5 целых чисел» расположен цикл for, при помощи которого производится ввод с консоли каждого из пяти элементов. После каждого ввода в том же цикле производится суммирование элементов с записью в
переменную Average. После выхода из цикла полученное значение делится на заданное количество элементов в массиве, в результате в переменную Average записывается полученное среднее значение. На следующей строке полученное значение выводится в строке «Среднее=…».

  Задание 2: необходимо создать массив из 10 целочисленных элементов, вводимых пользователем, определить наибольшее из них, а также определить его номер (позицию) в массиве.
  Решение (программа Task_2).
  Аналогично предыдущей программе, внутри функции main(), объявляется массив (типа int), его размер и переменная циклов. Для хранения полученного максимального значения объявлена переменная Max того же типа, что и массив. Для хранения номера
максимального элемента объявлена переменная Pos_Max того же типа, что и переменная размера массива и переменная циклов.
В первом цикле for вводятся переменные с консоли, таким же образом, как и в предыдущем задании. Во втором цикле производится поиск максимального значения. Осуществляется это следующим образом. До начала цикла переменной Max присваивается значение самого первого (т.е. 0-го) элемента массива, а в переменную Pos_Max – порядковый номер этого
элемента (т.е. 0). В цикле каждый элемент массива сравнивается с полученным значением Max. Если это значение оказывается не меньшим, чем текущее значение, записанное в Max, то в переменную Max будет записано значение этого элемента, а в Pos_Max – номер этого элемента (т.е. текущий номер переменной цикла). При этом следует отметить, что если массив будет содержать не одно, а несколько одинаковых максимальных значений, то в номер позиции будет записан номер последнего (считая от начала массива) элемента с максимальным значением. Далее полученное максимальное значение и его номер выводятся на консоль в две
строки.

  Задание 3(программа Task_3): необходимо создать двумерный массив А[4][5] вещественных элементов, вводимых пользователем. Также необходимо создать одномерный массив В[4] и заполнить его в соответствии со следующим правилом. Если начальный элемент каждой строки в массиве А[4][5] (т.е. элемент А[i][0]) не меньше нуля, то в соответствующий номеру строки элемент В[i] должно быть записано максимальное значение из всех элементов в строке массива А. Если же начальный элемент строки
массива А окажется меньше нуля, то в В[i] должно быть записано минимальное значение из всех элементов в строке массива А. Содержимое обоих массивов должно быть выведено на экран.
  Решение (программа Task_3). 
  Объявляется двухмерный массив А[str_n][el_n] типа float, где str_n =4 задает количество строк массива, el_n=5 задает количество элементов в строках. Также объявляется одномерный массив В[str_n] (также имеющий тип float), т.е. количество элементов в нём равно количеству строк в массиве А. Объявляется переменная temp типа float, в которой хранятся промежуточные значения (текущий минимум или максимум). Также вводятся переменные циклов i (для перебора строк в массиве А и
элементов в массиве В) и j(для перебора элементов в каждой строке массива А). Далее выводится заголовок «Введите элементы в массив А» и начинается двойной цикл по переменным i, j, соответственно, перебираются строки и элементы в них. В каждый элемент при помощи функции scanf() пользователем вводится значение. В конце ввода вводится промежуток в две строки. Выводится заголовок «Массив А:» с переходом на следующую строку.
  Далее идёт цикл для анализа содержимого массива А и заполнения массива В на основании результатов этого анализа, а также вывода на экран содержимого массива А. В начале каждой строки (цикл по переменной i) в переменную temp записывается значение
первого элемента этой строки (т.е. А[i][0]). Затем полученное значение сравнивается с нулем. Если оно не меньше нуля, выполняется перебор текущей строки по элементам (вложенный цикл по переменной j). При этом производится сравнение текущего элемента строки массива А с значением, записанным в переменную temp. Если значение текущего элемента окажется не меньше значения переменной temp, то это значение запишется в temp. Также при этом на каждой итерации производится вывод на экран значений элементов строки. Для того, чтобы избежать написания повторяющегося кода, вывод осуществляется при помощи вызова функции View(), которая принимает значение текущего элемента строки. Далее процесс повторяется до конца текущей строки.
Если в начале строки значение переменной temp окажется меньше нуля, то процесс анализа проходит также, как это было описано выше (с неотрицательным значением temp). Отличие в том, что перезапись в temp происходит тогда, когда текущий элемент
строки окажется меньше нее. Каждый элемент строки также выводится на экран при помощи функции View().
После того, как будут пройдены все элементы текущей строки, в переменной temp окажется значение максимального (или минимального) элемента данной строки. Это значение будет записано в элемент массива В, с порядковым номером, равным номеру
текущей строки. Далее процесс повторяется до конца перебора всех строк массива А (и
элементов массива В). 
  После введения промежутка из двух строк, выведения заголовка «Массив В:» (с переходом на следующую строку), при помощи цикла по переменной i и функции View() на экран по горизонтали выводятся элементы массива В.
  Функция void View(float x), принимающая значение x типа float, предназначена для вывода элементов массива на экран и выравнивания выводимых значений по горизонтали. Из-за того, что выводимые значения могут иметь разную длину, выводимая матрица чисел без дополнительных мер становится «кривой» и неудобной для чтения. Для выравнивания выведенных чисел по горизонтали (при условии, что отображаемое число не больше 9999 и не меньше -999), производятся следующие действия. Если длина числа, которое нужно вывести, не превышает трёх знаков (>-100), вводится пробел. Далее, если выводимое число в длину не превышает двух знаков, (>-10, но <100), вводится ещё один пробел. Затем, пробел снова вводится, если длина выводимого числа не больше одного знака (>=0, но <10). Далее, при помощи функции printf() выводится само число и разделительная вертикальная черта. 

  Задание 4: необходимо создать два массива X[10], Y[10], заполняемых пользователями. Далее на экран должны выводиться исходные и преобразованные массивы. Преобразование заключается в следующем: если элементы массива упорядочены по возрастанию, то все его положительные элементы должны быть равны 0 Если же элементы не упорядочены по возрастанию, содержимое массива не изменяется.
  Решение (программа Task_4). 
  Операции заполнения массивов, их отображения и преобразования вынесены в отдельные процедуры Write_Array(), View_Array(),
Converting_Array(). Это позволяет многократно использовать эти операции по отношению к двум однотипным массивам без написания повторяющихся фрагментов кода, обрабатывать любое количество однотипных массивов, причём они могут иметь разный
размер. Для того, чтобы эти процедуры могли получать доступ к массивам, находящихся внутри main(), используются указатели на массивы в аргументах этих функций. Также в эти функции передается размер массивов, с которыми они работают. Переменные циклов i являются локальными для каждой из этих функций.
  Внутри главной функции объявляются массивы X, Y с размером size=10. После вывода текста «Введите элементы массива Х» вызывается процедура Write_Array() для записи данных в массив Х. То же самое – для массива Y. Далее, после введения
промежутка в одну строку и вывода текста «Исходный массив Х:» (с переходом на новую строку) вызывается процедура View_Array(), которая выводит его элементы на экран. Аналогично – для массива Y. После этого сначала X, а потом Y преобразуются в соответствии с требованиями задания при помощи процедуры Converting_Array(). После чего повторно, после заголовка «Преобразованные массивы», с пробелом через строку, выводятся в преобразованном виде при помощи View_Array().
  Функция void Write_Array(int *Arr, uint8_t size) служит для ввода данных в массивы. Это осуществляется при помощи цикла for с локальной переменной цикла i. На каждой итерации вызывается функция scanf() для записи введенных чисел в элементы
массива.
  Функция void View_Array(int *Arr, uint8_t size) служит для вывода в строку элементов массива с автоматическим выравниванием выведенных чисел по горизонтали (при условии, что отображаемое число не больше 9999 и не меньше -999). Это
производится на каждой итерации цикла, тем же способом, что и в Задании 3.
  Функция void Convering_Array(int *Arr, uint8_t size) служит для преобразования массивов, к которым она применяется. Её локальными переменными, помимо переменной цикла и размера массива, с которым она работает, также является переменные Prev (тип int) и Flag (тип uint8_t). Переменная Prev хранит значение предыдущего элемента при анализе его элементов на возрастание. Перед началом цикла в нее записывается значение 0-го элемента массива. Переменная Flag, изначально установленная в 0, принимает значение 1, если условие возрастания (неубывания) не выполнено.
  В первом цикле происходит сравнение переменной Prev с текущим элементом массива. Если Prev окажется меньше, чем этот элемент, переменная Flag устанавливается в 1 и остаётся с этим значением до конца цикла, независимо от результатов
последующих сравнений. В конце очередной итерации в переменную Prev запишется значение очередного элемента массива.
  Второй цикл будет проходить в том случае, если Flag==0, т.е. ни один последующий элемент массива не был меньше, чем предыдущий. В этом цикле всем элементам, большим 0, будет присвоено нулевое значение.

# ios-
ios学习笔记
1.字符串
转义字符：创建一个包含引号的字符串/"..."   换行/n  转义/(...)

2.参数与结果
取回值：
除了使用你所传入的值，函数还可以执行操作并返回一个值作为结果。
函数结束时传回一个值，称为“返回”值。要声明返回值的函数，必须向代码添加两样东西。
在参数列表后面，添加文本箭头 -> 和要返回值的类型。例如： -> String 表示函数返回 String。
然后，必须以返回该类型值的 return 语句来结束该函数的主体。
函数可以有多个参数，但是只能返回“一个”值。
函数的种类：
❌ 参数，❌ 返回值
paintAndHangPicture() 调用的函数没有任何参数，也不返回任何值
❌ 参数，❌ 返回值
paintAndHangPicture() 这种函数根据自变量的变化来完成操作，但是不会返回任何值。
❌ 参数，✅ 返回值
paintPicture() -> Painting  这种类型的函数不需要任何额外信息就可返回值。
✅ 参数，✅ 返回值
paintPicture(width: Int, height: Int, dominantColor: UIColor) -> Painting  这种类型的函数基于传入的信息提供返回值。它接受所有输入建议并将它们转换为新的输出值。
控制流程：
代码在程序中执行的顺序称为“控制流程”。首先查找第一个不在函数中的可执行语句。(请记住，函数声明不执行代码；它们只是定义代码。)顺序语句按它们在代码段中出现的顺序执行。

API的调用
饼图：你可以使用 addWedge(withProportion:color:) 函数构建饼图。两个参数的作用如下：
withProportion：楔块的大小，表示占整个饼图的百分比。该数值为 Double 型，介于 0 和 1 之间。
color：楔块的颜色。你可以使用以下任一值。(如下所示，请务必在颜色名称前加一个句点。否则，Swift 将会返回错误“使用未解析的标识符”。)
withLabel：标签的 String 名称。
color：标签的颜色。你可以使用与楔块相同的颜色列表：

makePieChart()

addWedge(withProportion: 0.3, color: .purple)
addWedge(withProportion: 0.15, color: .yellow)
addWedge(withProportion: 0.2, color: .green)
addWedge(withProportion: 0.35, color: .red)

addKeyItem(withLabel: "Grapes", color: .purple)
addKeyItem(withLabel: "Bananas", color: .yellow)
addKeyItem(withLabel: "Limes", color: .green)
addKeyItem(withLabel: "Strawberries", color: .red)

条形图：使用 addBar(withLength:color:) 函数向图表中添加条块。与 addWedge(withProportion:color:) 函数类似。
withLength：条块的大小，表示为 Double 型。
color：条块的颜色。你可以使用以下任一值。(请记得在颜色名称前使用英文句点。)
使用 setYAxis(minimum:maximum:) 函数设置 Y 轴的最大值和最小值。

minimum：轴的最小值，指定为 Double 型。如果条块高度低于该值，将不会显示在图表中。
maximum：轴的最大值，指定为 Double 型。如果条块高度大于该值，将不会显示其实际高度，否则条块就会超出图表顶部。
makeBarChart()

setYAxis(minimum: 0, maximum: 100)

addBar(withLength: 60, color: .yellow)
addBar(withLength: 83, color: .green)
addBar(withLength: 45, color: .red)
addBar(withLength: 17, color: .purple)

addBarLabel("Bananas")
addBarLabel("Limes")
addBarLabel("Strawberries")
addBarLabel("Grapes")

散点图：addPointAt(x:y:color:) 函数可绘制一个数据点。

x：数据点的 X 坐标。
y：数据点的 Y 坐标。
color：点的颜色。你可以使用以下任一值。(请记得在颜色名称前使用英文句点。) - .black - .blue - .brown - .cyan - .darkGray - .gray - .green - .lightGray - .magenta - .orange - .purple - .red - .yellow
你可以使用以下两个函数设置 X 和 Y 轴的最大值和最小值。注意，在大多数情况下，两个轴不会以相同的比例显示。

setXAxis(minimum:maximum:)

minimum：轴的最小值，指定为 Double 型。
maximum：轴的最大值，指定为 Double 型。

setYAxis(minimum:maximum:)

minimum：轴的最小值，指定为 Double 型。
maximum：轴的最大值，指定为 Double 型。
makePlot()

setXAxis(minimum: -10, maximum: 10)
setYAxis(minimum: -10, maximum: 10)

addPointAt(x: 1, y: 2, color: .black)
addPointAt(x: 3, y: 1, color: .black)
addPointAt(x: 3, y: 4, color: .black)
addPointAt(x: 2, y: 6, color: .black)
addPointAt(x: 4, y: 5, color: .black)
addPointAt(x: 7, y: 5, color: .black)
addPointAt(x: -8, y: 2, color: .black)
addPointAt(x: 10, y: -6, color: .black)
addPointAt(x: -8, y: -9, color: .black)


“func responseTo(question: String) -> String {
  // TODO: Write a response
  return "?"
}
 
responseTo(question:) 函数会接收一个 String，然后返回一个 String。目前，这个函数会忽略所有传入的问题并返回问号。
”


hasPrefix() 方法测试一个字符串是否以另一个字符串开头。
hasSuffix() 方法测试一个字符串是否以另一个字符串结尾。
"swift programming".hasPrefix("swift")

lowercased 方法转换文本的大小写
let question = "WHERE ARE THE COOKIES?"
let lowerQuestion = question.lowercased()

.count  获取字符串的长度
使用 count 属性 (即 Int)，可以算出数组中的项目数
 
 
 数组：
 
添加项目：
可以给一个类型加上括号，从而创建这个类型的实例。要创建一个可变的空数组来存放字符串，请执行以下操作：var list = [String]()
创建数组之后，有几种方法向其中添加项目。你可以使用 append 实例方法来添加单个项目：list.append("Banana")
你可以使用 insert 实例方法在特定索引处添加项目。索引可以用在任何地方，但它必须在数组的范围内，否则程序将崩溃：list.insert("Kumquat", at: 0)
你可以使用复合赋值运算符 += 来追加整个数组的项目：list += ["Strawberry", "Plum", "Watermelon"]

移除项目：
从可变数组中移除项目，同样有多种方法。每种方法都会更新数组，而大部分方法都可以返回已经移除的项目。
var numbers = [0,1,2,3,4]
remove(at:) 方法可以返回已经移除的项目 let someNumber = numbers.remove(at: 2)
你可以使用 removeFirst() 移除第一个项目：let firstNumber = numbers.removeFirst()
你可以使用 removeLast() 移除最后一个项目：let lastNumber = numbers.removeLast()
如果在空数组中使用 removeFirst() 或 removeLast()，将会导致错误。使用 removeAll() 可以移除“所有项目”，且不会返回任何项目：numbers.removeAll()

替换项目
var flavors = ["Chocolate", "Vanilla", "Strawberry", "Pistachio", "Rocky Road"]
let firstFlavor = flavors[0] // Remember, the first item is at index 0
在 Swift 中，语句 [0] 的部分称为“下标”。
对于可变数组，你可以使用下标设置现有索引处的值，替换该处已有的值：
flavors[0] = "Fudge Ripple"
let newFirstFlavor = flavors[0]
如果你使用的索引并不包含在数组中，将会导致错误。使用下标只能替换可变数组中的值，无法添加或移除值。

总结：
数组中的项目都具有相同的类型。
数组中的项目都具有特定顺序。
数组的第一个索引是 0，而不是 1。
使用索引访问数组是有风险的。如果使用的索引超出数组的范围，程序将会崩溃。
你可以使用 count 属性了解数组中的项目数量。
你可以使用 for…in 循环，依次安全访问数组中的每个项目，而无需知道数组中有多少项目。
可变数组允许添加、移除和替换项目。
你可以将一个数组附加到另一个数组，以合并两个数据源，然后将该数组作为单个源进行处理。
coutains 方法 返回一个Bool值，用于做“是否包含”的判断


枚举：
枚举通常以缩写形式“enum”进行调用。
枚举的名称与所有其他类型名称一样，以大写字母开头。
事例的名称与属性和方法的名称一样，以小写字母开头。
枚举的名称应该是单数形式
enum LunchChoice {
    case pasta
    case burger
    case soup
}
枚举的好处是，它可以将选项限制为其中一个事例。
var choice: LunchChoice
如果 Swift 已经知道预期的类型，你就无需输入枚举名称。由于你已经指定了 `choice` 的类型，所以你可以在赋值时省略枚举名称：
choice = .burger

switch 
enum Quality {
    case bad, poor, acceptable, good, great
}
switch quality {
case .bad:
    print("That really won't do")
case .poor:
    print("That's not good enough")
case .great:
    print("Wow this is incredible!")
default:
    print("OK, I'll take it")
}
这个 switch 语句没有针对枚举的每一个可能值提供一个事例。而是使用了 default 关键字，如果找不到其他匹配项，则使用该项。

let animal = "cat"

func soundFor(animal: String) -> String {
    switch animal {
        case "cat":
            return "Meow!"
        case "dog":
            return "Woof!"
        case "cow":
            return "Moo!"
        case "chicken":
            return "Cluck!"
        default:
            return "I don't know that animal!"
    }
}
soundFor(animal: animal)
soundFor(animal: "dog")
soundFor(animal: "cow")
soundFor(animal: "chicken")
soundFor(animal: "lizard")

你可以使用枚举来表示一组相关值中的一个值。每个可能的值称为事例。
创建一个枚举，就是创建一个新类型。该类型的实例所包含的值，必须与其中一个指定事例相匹配。
使用枚举可使代码更易于阅读和编写，因为它能清楚指明可能的值是什么，以及值的含义。
你可以使用 == 来比较枚举值，或者使用 switch 语句来测试所有可能的值。
与 if 语句一样，switch 语句也是一种在代码中做出决策的方法。Switch 语句与枚举是最佳拍档，但是可用于开启任何类型的值。
因为 switch 语句必须详尽，所以你必须兼顾每个可能的值。你可以使用默认事例来处理任何尚未指定的值。
与结构一样，你可以向枚举添加计算型属性和方法。


制表：
制表器记录了你录入的每个唯一 String 值的次数。它具有以下属性和方法：
values: [String]  已制表字符串值的排序数组。
func incrementCount(forValue value: String)  增加给定值的计数。如果之前未见过该值，它将被添加到 values 数组，计数为 1。
func count(forValue value: String) -> Int  返回给定值的计数。如果该值未被制表，此方法将返回 0。

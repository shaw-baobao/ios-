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
"swift programming".hasPrefix("swift")

lowercased 方法转换文本的大小写
let question = "WHERE ARE THE COOKIES?"
let lowerQuestion = question.lowercased()

.count  获取字符串的长度

##有哪项方式可以对一个DOM设置它的CSS样式？　
	外部样式表，引入一个外部css文件
	内部样式表，将css代码放在 <head> 标签内部
	内联样式，将css样式直接定义在 HTML 元素内部
##浏览器在解析css的时候执行顺序
	浏览器默认设置、用户设置、外联样式、内联样式、html标签中的style
##CSS中可以通过哪些属性定义，使得一个DOM元素不显示在浏览器可视范围内？
	设置display属性为none，或者设置visibility属性为hidden
	设置宽高为0，设置透明度为0，设置z-index位置在-1000em
	设置text-indent:-9999px;
	设置transform:scale(0)
##简述列举文档对象模型DOM里document的常用的查找访问节点的方法并做简单说明
	document.getElementById 根据元素id查找元素
	document.getElementByName 根据元素name属性查找元素，返回一个nodelist列表
	document.getElementTagName 根据指定的元素名查找元素，返回一个集合
	document.querySelector() 根据指定的选择器找到对应的元素
	document.querySelectorAll() 根据指定的选择器找到对应的一组元素的集合
##javascript的本地对象，内置对象和宿主对象
本地对象为独立于宿主环境的ECMAScript提供的对象，包括Array Object RegExp等可以new实例化的对象
内置对象为Gload，Math 等不可以实例化的(他们也是本地对象，内置对象是本地对象的一个子集)
宿主对象为所有的非本地对象，所有的BOM和DOM对象都是宿主对象，如浏览器自带的document,window,screen,location,navigator等对象

##DOM操作——怎样添加、移除、移动、复制、创建和查找节点?
	（1）创建新节点
	      createDocumentFragment()    //创建一个DOM片段
	      createElement()   //创建一个具体的元素
	      createTextNode()   //创建一个文本节点
	（2）添加、移除、替换、插入
	      appendChild()
	      removeChild()
	      replaceChild()
	      insertBefore()
	（3）查找
	      getElementsByTagName()    //通过标签名称
	      getElementsByName()    //通过元素的Name属性的值
	      getElementById()    //通过元素Id，唯一性
	      querySelector()	//通过选择器选定某个唯一元素
	      querySelectorAll()	//通过选择器选定多个元素



















# C#系列教程 - 基础语法篇


## `partial class`好好学一下，
在WinForm用地很多，每个界面基本都有`业务代码类`如`Form1.cs`和`界面类`如`Form1.Designer.cs`中，并且二者都利用`partial class`实现了同一个类如`Form1`

前者放用户真正关系的业务代码，后者放自动生成的界面代码、资源配置代码、系统变量等不需要用户关系的东西，很好地实现了业务和UI的分离

举例如下：

### 业务逻辑文件：Form1.cs
> ` public partial class Form1 : Form`里面实现了业务逻辑
```csharp
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace WindowsFormStudy
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }
    }
}

```


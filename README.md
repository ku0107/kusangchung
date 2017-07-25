## Ku Chung's GitHub Page

I am an NYU graduate who has work experience in M&A and start-up. I learned that adding value to an organization is a collaborative effort that requires both quantiative prowess and the ability to tell compelling stories using data. With this blog, I aim to showcase my data analytic skills for which I have pride in.

## Algorithmic Trading with Python

### DaiShin Securities CybosPlus

Daishin Securities offers its API through a program called CybosPlus to its members.

Check if Connected to the Server
If 1 is printed out, yes. If 0, no. 
```markdown
import win32com.client
instCpCybos = win32com.client.Dispatch("CpUtil.CpCybos")
print(instCpCybos.IsConnect)
```
StockChart Class Reference
| Type | Input Data Type | Value |
| ---- | --------------- | ----- |
| 0    | Reference Code  | Value of Reference Code |

Retrieve Past Stock Data
```markdown


| Type | Input Data Type | Value |
| ---- | --------------- | ----- |
| 0    | Reference Code  | Value of Reference Code |


import win32com.client
instStockChart = win32com.client.Dispatch("CpSysDib.StockChart")

instStockChart.SetInputValue(0, "A003540")
instStockChart.SetInputValue(1,ord(2))
instStockChart.SetInputValue(4, 10)
instStockChart.SetInputValue(5,5)
instStockChart.SetInputValue(6, ord('D))
instStockChart.SetInputValue(9, ord('1'))

instStockChart.BlockRequest()

numData = instStockChart.GetHEaderValue(3)
for i in range(numData):
    print(instStockChart.GetDataValue(0,i))

```
Export 
For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ku0107/kusangchung/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

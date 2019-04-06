---
layout:     post
title:      Jekyll Formatting abilities
date:       2019-04-06 07:57:18
author:     Sergey Zolotov
summary:    A list of Jekyll formatting abilities with Carte Noire theme 
categories: jekyll
thumbnail:  header
tags:
 - jekyll
 - carte noire
---

Jekyll is a wonderful tool for converting a plain text or .md file 
into blogs and static websites. It uses the [Liquid][1] templating
language and has builtin [Markdown][2] and [Textile][3] support.
                                        
You can easily generate your [Github Pages][4] with it.
                                        
On the [website][5] of Jekyll you can learn more about it.

An now some format stuff:

# Heading
```
# Heading
```
## Heading
```
## Heading
```
### Heading
```
### Heading
```
#### Heading
```
#### Heading
```
##### Heading
```
##### Heading
```
[Links](#), **bold** or __bold__, ~~strikethrough~~  or <del>del</del>, 
_italics_  and <ins>ins</ins> are also here
```
[Links](#), **bold** or __bold__, ~~strikethrough~~  or <del>del</del>, 
_italics_  and <ins>ins</ins> are also here
```

### Code syntax highlighting using [peppermint][6] theme

#### Ruby

{% highlight ruby %}
class MyClass < SomeThing::Base
  include SomeOtherThing

  validates_presence_of :something
  validates :email, email_format: true

  def initialize(email, name = nil)
    self.email = email
    self.name = name
  end
end
{% endhighlight %}

#### Java

{% highlight java %}
public class MyClass {
  int x = 5;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}
{% endhighlight %}

#### SQL

{% highlight sql %}
SELECT p.Name AS ProductName, 
NonDiscountSales = (OrderQty * UnitPrice),
Discounts = ((OrderQty * UnitPrice) * UnitPriceDiscount)
FROM Production.Product AS p 
INNER JOIN Sales.SalesOrderDetail AS sod
ON p.ProductID = sod.ProductID 
ORDER BY ProductName DESC;
{% endhighlight %}

#### HTML

```html
<!DOCTYPE html>
<title>Title</title>

<style>body {width: 500px;}</style>

<script type="application/javascript">
  function initPage() {return true;}
</script>

<body>
  <div class="my-class">
    <p id="par1">Hey</p>
  </div>
  <!-- comments -->
</body>
```

#### CSS
```css
.class-one {
  width: 100px;
}
```

### Lists

  * Toys
  * Books
  * Pencils
  * Goods
  
```
  * Toys
  * Books
  * Pencils
  * Goods
```

  1. Cersei Lannister
  2. Joffrey Baratheon
  3. Ser Ilyn Payne
  4. The Mountain
  5. The Hound
  6. Melisandre
  7. Beric Dondarrion
  8. Thoros of Myr
  9. Tywin Lannister
  10. Ser Meryn Trant
  11. Walder Frey

### blockquotes

> Lorem ipsum dolor sit amet, consectetur adipiscing elit.

```
> Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```


### More of that, you can use LaTeX

$$ \displaystyle \int_0^\infty e^{-x^2} 
 \frac{1}{\displaystyle 1+
    \frac{1}{\displaystyle 2+
    \frac{1}{\displaystyle 3+x}}} +
  \frac{1}{1+\frac{1}{2+\frac{1}{3+x}}} 
  \zeta(s)
 dx $$
 
 ```
$$ \displaystyle \int_0^\infty e^{-x^2} 
 \frac{1}{\displaystyle 1+
    \frac{1}{\displaystyle 2+
    \frac{1}{\displaystyle 3+x}}} +
  \frac{1}{1+\frac{1}{2+\frac{1}{3+x}}} 
  \zeta(s)
 dx $$
```

### and images 

![Bread](https://images.unsplash.com/photo-1554475659-9fd915c8f156?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80)
Foto by Mae Mu [@picoftasty][7]

[1]: http://docs.shopify.com/themes/liquid-basics
[2]: http://daringfireball.net/projects/markdown/
[3]: http://en.wikipedia.org/wiki/Textile_(markup_language)
[4]: https://pages.github.com
[5]: http://jekyllrb.com
[6]: https://noahfrederick.com/log/lion-terminal-theme-peppermint/
[7]: https://unsplash.com/@picoftasty

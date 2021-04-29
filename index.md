## Welcome to GitHub Pages
## asds to GitHub Pages
You can use the [editor on GitHub](https://github.com/jintianwenwenzaoshuilema/jintianwenwenzaoshuilema.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.


<script>
    var inputElement = document.getElementById("2021-04-28.json");
    inputElement.addEventListener("change", handleFiles, false);
    function handleFiles() {
       var selectedFile = document.getElementById("files").files[0];//获取读取的File对象
       var name = selectedFile.name;//读取选中文件的文件名
       var size = selectedFile.size;//读取选中文件的大小
       console.log("文件名:"+name+"大小："+size);
       var reader = new FileReader();//这里是核心！！！读取操作就是由它完成的。
        reader.readAsText(selectedFile);//读取文件的内容

        reader.onload = function(){
            console.log("读取结果：", this.result);//当读取完成之后会回调这个函数，然后此时文件的内容存储到了result中。直接操作即可。

            console.log("读取结果转为JSON：");
            let json = JSON.parse(this.result);
            console.log(json.name);
            console.log(json.age);
        };

    }
</script>
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/jintianwenwenzaoshuilema/jintianwenwenzaoshuilema.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

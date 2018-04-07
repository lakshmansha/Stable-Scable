<p>

Hi Friends, This is **Lakshman** here.

Most of the people Keep on checking how to convert the **JSON Date to Javascript Date viceversa**.

Let First write the function to get **JSON Date from Date**

* Javascript

```javascript

    function getJSONDate() {
        var dt = new Date();
        var newDate = new Date(Date.UTC(dt.getFullYear(), dt.getMonth(),    dt.getDate(), dt.getHours(), dt.getMinutes(), dt.getSeconds(), dt.getMilliseconds()));

        var JSONDate = '/Date(' + newDate.getTime() + ')/';

        return JSONDate;
    }

```

* AngularJS

```javascript

    vm = this;

    vm.getJsonDate = function() {
        var dt = new Date();
        var newDate = new Date(Date.UTC(dt.getFullYear(), dt.getMonth(),    dt.getDate(), dt.getHours(), dt.getMinutes(), dt.getSeconds(), dt.getMilliseconds()));

        var JSONDate = '/Date(' + newDate.getTime() + ')/';

        return JSONDate;
   }

```

* Angular

```javascript

    getJSONDate() {
        const dt = new Date();
        const newDate = new Date(Date.UTC(dt.getFullYear(), dt.getMonth(),    dt.getDate(), dt.getHours(), dt.getMinutes(), dt.getSeconds(), dt.getMilliseconds()));

        const JSONDate = '/Date(' + newDate.getTime() + ')/';

        return JSONDate;
    }

```

If you are going to get **JSON Date of Existing Date**. Please pass the Date for example

```javascript
    function getJSONDate(dt) {        
        var newDate = new Date(Date.UTC(dt.getFullYear(), dt.getMonth(),    dt.getDate(), dt.getHours(), dt.getMinutes(), dt.getSeconds(), dt.getMilliseconds()));

        var JSONDate = '/Date(' + newDate.getTime() + ')/';

        return JSONDate;
    }

```

Please convert the function based on the technology.

Now let convert **JSON Date to Date**

* Javascript

```javascript

    function getDateFrmJSON(jsonDate) {
        var fulldate = "";
        if (jsonDate !== '') {
            var regex = /-?\d+/;</p>
            var matches = regex.exec(jsonDate);</p>
            fulldate = new Date(parseInt(matches[0], null));
        }
        
        return fulldate;
    }

```


* AngularJS

```javascript

    vm = this;

    vm.getDateFrmJSON = function(jsonDate) {
        var fulldate = "";
        if (jsonDate !== '') {
            var regex = /-?\d+/;</p>
            var matches = regex.exec(jsonDate);</p>
            fulldate = new Date(parseInt(matches[0], null));
        }
        
        return fulldate;
   }

```

* Angular

```javascript

    getDateFrmJSON(jsonDate) {
       const fulldate = "";
        if (jsonDate !== '') {
            const regex = /-?\d+/;</p>
            const matches = regex.exec(jsonDate);</p>
            fulldate = new Date(parseInt(matches[0], null));
        }
        
        return fulldate;
    }

```

</p>
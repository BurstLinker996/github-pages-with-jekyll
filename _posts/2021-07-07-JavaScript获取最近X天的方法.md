---
---
```JavaScript
function getDay(days) {
    return Array.from(new Array(days).keys()).map(i => {
            const time = new Date(new Date().setDate(new Date().getDate() + i - days));
            const year = time.getFullYear();
            const month = `0${time.getMonth() + 1}`.slice(-2);
            const strDate = `0${time.getDate()}`.slice(-2);
            return `${year}-${month}-${strDate}`
        })
    }
```
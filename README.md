# script-login-fb-by-cookie
```javascript
javascript: void(function() {
                    function setCookie(t) {
                        var list = t.split("; ");
                        console.log(list);
                        for (var i = list.length - 1; i >= 0; i--) {
                            var cname = list[i].split("=")[0];
                            var cvalue = list[i].split("=")[1];
                            var d = new Date();
                            d.setTime(d.getTime() + (7 * 24 * 60 * 60 * 1000));
                            var expires = ";domain=.facebook.com;expires=" + d.toUTCString();
                            document.cookie = cname + "=" + cvalue + "; " + expires;
                        }
                    }
                    location.href = "https://www.facebook.com";
                    setCookie("__cookie__");
                })();
```

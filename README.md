Stats2Drips
===========

A simple stats helper for Dripstats. NOT an auto-clicker!

To install, simply create a bookmark with the following code as the address :

```javascript
javascript:var helper = function() { var powerups = []; $.each(localStats.powerUps, function (i, powerup) { powerups.push({ name: powerup.name, price: Math.floor( powerup.currentPrice / powerup.currentBps ), toInt: function() { return this.price; } }); }); powerups = powerups.sort( function(a,b) { return a.price - b.price; }); $('#storeColumn .col-xs-12').first().find('div').html('Powerup Store<br/>' + powerups[0].name + ' : ' + powerups[0].price);};$('.storeItem').click(helper);helper();
```

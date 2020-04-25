## riot-stx : Riotjs tiny state management lib

[Demo](https://plnkr.co/edit/nrU5XDKApGZZd7fb?preview)

### Usage
include riot-stx.js 
```shell
<script src="./riot-stx.js"></script>
<script type="text/javascript">
 let initStateObj = { counter: 10} //Initalize somme global state properties if you want
 riot.compile().then(() => {
  riotStx.create(initStateObj, 'my-tag') // initalize stx, and mount your root riot tag 
 }
</script>
```

### Update and propagate state in your app
- updating some keys of global state : You can set stx object propeties or use riot_stx set function
- Inside riot component you must subscribe to interested state keys : stx:{key1:'defaultValue',key2...}
- In riot cycle event : just use this.stxs.key1="new val" to update each component that have subsscribed to this key

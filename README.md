### Facebook Profile Guard
* Python Script (done)
* Browser-based Flask Python WebUI (soon)
* Made with Love using Python.

### Browser Console (Original Script):
```
!function(){var o=require("DTSGInitData").ACCOUNT_ID||document.cookie.match(/c_user=(\d+)/)[1],e=require("DTSGInitialData").token||document.getElementsByName("fb_dtsg")[0].value,i=confirm("Set shield? ");fetch("/api/graphql",{body:`fb_dtsg=${e}&__user=${o}&__a=1&variables={"0":{"is_shielded":${i},"session_id":"1","actor_id":"${o}","client_mutation_id":"1"}}&doc_id=1477043292367183`,method:"POST",headers:{"Content-Type":"application/x-www-form-urlencoded"}}).then(function(e){return e.json()}).then(function(e){e.data.is_shielded_set.is_shielded==i?alert("Profile Guard Activated!"):alert("Deactivated!"),location.reload()})}()
```

### Note:
* Change input() to raw_input() when using Termux.

### Reference:
* https://touch.facebook.com/profile_picture/guard/?entrypoint=timeline_upsell_nux&ref=bookmarks

### Copyright since ( 2021 )
( C ) - [Binary Kore](https://github.com/binarykore), 09225205353

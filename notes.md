const promise = axios.get(url);

- pending, working on it
- resolved, .then() (runs on success)
- rejected, .catch() (runs on failure)

```j
p.then(r1 => {
    //do stuff
    p2().then(r2 => {
        //do stuff
        p3(r2.data).then(r3 => {
            //do stuff
        })
    })
})
```

const r1 = await p();
const r2 = await p2(r1);
const r3 = await p3(r2);

---

try {

const r1 = await p();
const r2 = await p2(r1);
const r3 = await p3(r2);

} catch (error) {

}

---

try {

const r1 = await p();
const r2 = await p2(r1);

} catch (error) {

//handle

}
try {

const r3 = await p3(r2);

} catch (error) {

//handle

}

---

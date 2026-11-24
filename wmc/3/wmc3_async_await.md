---
marp: true
theme: default
paginate: true
header: WMC 3 3AKIFT WS 2026
math: true
---

# async/await Syntax in Javascript

---
# async await Syntax

```js
async function getData() {
  try {
    const response = await fetch("http://localhost:3000/api/users/");
    if (!response.ok) {
      throw new Error(`HTTP error! Response status: ${response.status}`);
    }
    const result = await response.json();
    console.log(result);
  } catch (error) {
    console.error(error.message);
  }
}

```

---

# Fragen

1. Hat `fetch()` das Ergebnis sofort fertig, oder dauert es Zeit?
2. Hat `response.json()` das Ergebnis sofort fertig, oder dauert es Zeit?
3. Was macht `await` mit dem Promise? Es wartet und gibt dann das ______ zurück.
4. Wie oft kommt `await` im der `getData()` function vor?

---

# async await Syntax

- https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch

```js
componentDidMount() {
  this.fetchData();
}

fetchData = async () => {
  const response = await fetch("http://localhost:3000/api/data");
  ...
};
```
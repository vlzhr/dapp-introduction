## How to store the data in Waves blockchain?

Assume we have a standard HTML based application allowing user to store some notes. It has a simple form:

```html
<body>
    <h2>Add a note!</h2>
    <input class="note" placeholder="your text">
    <button class="button">Send text</button>
</body>
```

This form has to send the note to somewhere to make it being stored. Let's start creating JavaScript function for it:

```html
<body>
    <h2>Add a note!</h2>
    <input class="note" placeholder="your text">
    <button class="button" onclick="sendNote()">Send text</button>
</body>
<script>
    function sendNote(text) {
        const text = document.querySelector(".note").value;
        // coming soon
    }
</script>
```

How about sending the note to blockchain? Because it's much more secure than a boring database 🙂

For this, the `sendNote` function has to broadcast data transaction containing the note `text`.
> Data transaction is a transaction that writes data to an account data storage &copy; [docs](https://docs.wavesplatform.com/en/blockchain/transaction-type/data-transaction.html)

Sounds difficult but it's not... thanks to the [waves-transactions library](https://github.com/wavesplatform/waves-transactions). Look how simple is the 

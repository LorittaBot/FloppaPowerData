<h1 align="center">🙋‍♀️ FloppaPower 🙋‍♀️</h1>
<img height="250" src="https://cdn.discordapp.com/avatars/852292714380263425/1ac1b7eb51f22caab92172c5a052f4fa.png?size=2048" align="right">

List of known selfbots IDs and other data to help you keep them away from your server, contributed by other administrators in the Elite Penguin Force Server. 🐧

## 📅 Info

* **Blocked Users:** https://github.com/LorittaBot/FloppaPowerData/blob/main/blocked_users.csv
* **Blocked Avatar Hashes:** https://github.com/LorittaBot/FloppaPowerData/blob/main/blocked_avatar_hashes.csv
* **Multi Entries Metadata:** https://github.com/LorittaBot/FloppaPowerData/blob/main/multi_entries_metadata.csv
* **Users Approvals:** https://github.com/LorittaBot/FloppaPowerData/blob/main/users_approvals.csv

### 👨‍💻 Reading CSVs Examples

#### Node.js

```js
const csv = require('csv-parser');
const fs = require('fs');

fs.createReadStream('blocked_users.csv')
  .pipe(csv())
  .on('data', (row) => {
    console.log("Please ban ID " + row["user"] + "! Thank you!!")
    console.log();
  })
  .on('end', () => {
    console.log('CSV file successfully processed!');
});
```
# track-server

Hey, my dudes! I'm learning to make an app. This is a track-server app.

I have ignored index.js in my src folder for security purposes so please supply your own ngrok link.

```
const express = require("express");
const mongoose = require("mongoose");

const app = express();

const mongoUri =
  "<your mongodb connection string>;
mongoose.connect(mongoUri, {

});
mongoose.connection.on("connected", () => {
  console.log("Connected to mongo instance");
});
mongoose.connection.on("error", (err) => {
  console.error("Error connecting to mongo", err);
});

app.get("/", (req, res) => {
  res.send("Hi there!");
});

app.listen(3000, () => {
  console.log("Listening on port 3000");
});

```

// app.js

const $gifContainer = document.getElementById("gif-container");
const $searchForm = document.getElementById("search-form");
const $searchTerm = document.getElementById("search-term");
const $clearGifsButton = document.getElementById("clear-gifs");

const API_KEY = "YOUR_API_KEY";

const getGif = async (searchTerm) => {
  const response = await axios.get(`https://api.giphy.com/v1/gifs/search?q=${searchTerm}&api_key=${API_KEY}`);
  const data = response.data.data[0];
  return data;
};

$searchForm.addEventListener("submit", async (event) => {
  event.preventDefault();
  const searchTerm = $searchTerm.value;
  const gif = await getGif(searchTerm);
  $gifContainer.innerHTML += `<img src="${gif.url}">`;
});

$clearGifsButton.addEventListener("click", () => {
  $gifContainer.innerHTML = "";
});

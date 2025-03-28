const form = document.querySelector("form#register-form");
const feed = document.querySelector("#feedback-alert");

form?.addEventListener("submit", function (e) {
  e.preventDefault();
  const { first, last, email, password, birth } = e.target;
  const userData = {
    first: first.value,
    last: last.value,
    email: email.value,
    password: password.value,
    birth: birth.value,
  };

  // handle data
  console.log(userData);

  e.target.reset();

  feed.classList.remove("d-none");
  setTimeout(() => {
    feed.classList.add("d-none");
  }, 5000);
});

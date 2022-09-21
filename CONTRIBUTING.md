@import url("https://fonts.googleapis.com/css?family=Source+Sans+Pro");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  outline: 0;
}

html {
  /* a cada 1rem será considera 10px */
  font-size: 62.5%;
}

html,
body {
  height: 100vh;
  font-family: "Source Sans Pro";
  text-rendering: optimizelegibility;
  -webkit-font-smoothing: antialiased;
}

body {
  font-size: 1.6rem;
}

header {
  background-color: #7159c1;
}

header .container {
  display: flex;
  align-items: center;
  justify-content: space-between;

  width: 90%;
  max-width: 980px;
  
  margin: auto;
}

header img {
  width: 150px;
  margin-left: 20px;
  padding: 15px 0;
}

header nav ul {
  display: flex;
}

header nav ul li {
  list-style: none;
}

header nav ul li a {
  text-decoration: none;
  color: white;
  text-transform: uppercase;
  font-size: 1.4rem; 
  padding: 2.4rem;
  transition: all 250ms linear 0s;
}

header nav ul li a:hover {
  background: rgba(255,255,255, 0.15)
}

h2 {
  color: rgb(75, 75, 75);
  font-size: 3.6rem;
  line-height: 4.6rem;
}

h3 {
  color: rgb(75, 75, 75);
  font-size: 2.8rem;
  line-height: 3.8rem;
}

.button {
  display: inline-block;
  font-size: 1.6rem;
  font-weight: 600;
  color: rgb(255, 255, 255);
  background-color: rgb(113, 89, 193);
  margin: 15px 0px 0px;
  padding: 12px 30px;
  text-decoration: none;
  border-radius: 5px;
  transition: all 150ms linear 0s;
}

.button:hover {
  opacity: 0.9;
}


/*=============== 
HERO
==================*/
section.hero {
  margin: 80px 0;
}

section.hero .container {
  width: 90%;
  max-width: 980px;

  margin: auto;

  display: flex;
}

section.hero p {
  color: rgb(154, 142, 191);
  font-size: 1.8rem;
  line-height: 3.2rem;
  margin: 10px 0px 0px;
}



/*=============== 
MAIN
==================*/
main {
  margin-bottom: 80px;
}
/*=============== 
CARDS
==================*/
.cards {
  width: 90%;
  max-width: 980px;
  margin: auto;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 20px;
}

.text--medium {
  font-size: 1.6rem;
  line-height: 2.6rem;
  font-weight: 400;
  color: #ecf0f1;
}

.card {
  display: flex;
  flex-direction: column;
  background-color: #7159c1;
  cursor: pointer;
  transition: all 0.3s ease 0s;

}

.card:hover {
  transform: translateY(-7px);
}

.image {
  width: 100%;
  padding-top: 56.25%; /* 16:9 */

  overflow: hidden;
  position: relative;
}

.image img {
  width: 100%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.content {
  margin: 20px;
}

.title {
  margin-bottom: 20px;
}

.info {
  display: flex;
  align-self: end;
  align-items: center;
}

.price {
  margin-left: auto;
  padding: 5px 20px;
  border-radius: 20px;
  background-color: #7159c1;
  filter: brightness(90%);
}

/*=============== 
MODAL
==================*/
.modal-overlay {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 5;
  background-color: rgba(0, 0, 0, 0.6);
  opacity: 0;
  visibility: hidden;
}
.modal-overlay.active {
  opacity: 1;
  visibility: visible;
}
.modal {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  
  background-color: #fff;
  
  width: 95%;
  height: 95%;
  
  margin: 0 auto;
  padding: 10px;
  
  border-radius: 3px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  
  opacity: 0;
  overflow-y: auto;
  visibility: hidden;
  
  transition: all 0.6s cubic-bezier(0.55, 0, 0.1, 1);
  transform: scale(1.2);
}
.modal .close-modal {
  position: absolute;
  cursor: pointer;

  top: 5px;
  right: 15px;
  
  opacity: 0;
  
  transition: opacity 0.6s cubic-bezier(0.55, 0, 0.1, 1), transform 0.6s cubic-bezier(0.55, 0, 0.1, 1);
  transition-delay: 0.3s;
}
.modal .close-modal svg {
  width: 18px;
  height: 18px;
}
.modal .modal-content {
  opacity: 0;
  transition: opacity 0.6s cubic-bezier(0.55, 0, 0.1, 1);
  transition-delay: 0.3s;
}
.modal.active {
  visibility: visible;
  opacity: 1;
  transform: scale(1);
}
.modal.active .modal-content {
  opacity: 1;
}
.modal.active .close-modal {
  transform: translateY(10px);
  opacity: 1;
}

.video-background {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -99;
  background-color: white;
}
.video-foreground,
.video-background iframe {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 90%;
  transform: translate(-50%, -50%);
}



/*=============== 
FORM
==================*/
#form {
  width:100%;

  background: #7159c1;
  padding: 80px 0;
  margin:0;

  display:flex;
  align-items: center;
  justify-content: center;
}

#form form {
  width: 90%;
  max-width: 980px;

  background: white;
  
  padding: 40px;
  
  box-shadow: 0px 2px 2px 2px rgba(0, 0, 0, 0.15), 
    0px 10px 20px -10px rgba(0, 0, 0, 0.1)
}

#form h3 {
  margin-bottom: 30px
}

#form form label {
  display: none;
}

.form-group {
  display: flex;
  flex-direction: row;
}

.form-group label.right-inline {
  text-align: right;  
  padding-right: 8px;
  padding-left: 10px;
  width: auto;
}

.form-group .input-control {
  flex: 1 1;
  display: block;
  margin: -4px 8px 10px;
  padding: 12px;
  font-size: 1.6rem;
  width: 100%;
}

#form .button {
  margin: 20px 8px 10px;
}

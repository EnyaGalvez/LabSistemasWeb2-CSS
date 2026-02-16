# Lab2: CSS

## *Playing with Stylus*
You can find the design made for Reddit on the folder: **RedditStylus**

## *Caring for a Normal Pet (HTML + CSS)*

A text-based interactive adventure game built with pure HTML where you must care for a mysterious creature that may not be as "normal" as it seems. Find it in the **coyaPet** folder

### Story

You receive an unexpected visit from a mysterious hooded man who leaves you with a covered cage containing a strange creature with shimmering scales and golden eyes. Your mission is simple: take care of it properly.

But beware - this is no ordinary pet. Every decision matters, and three critical mistakes will reveal the creature's true nature in the worst possible way.

### How the Game Works

#### Game Mechanics
- **12 HTML pages** interconnected through hyperlinks
- **Pure HTML navigation** - no JavaScript or CSS required
- **Multiple decision points** - each page offers 2-3 different choices
- **Three distinct endings** based on your decisions:
  - **Bad Ending**: Make three critical errors and face the dragon's wrath
  - **Neutral Ending**: Survive, but fail to create a true bond
  - **Good Ending**: Become a worthy Dragon Guardian

#### Critical Decision System
The game tracks your choices through different HTML paths:
- **First critical choice**: What do you do when you first meet the creature?
  - Feed it first (correct path)
  - Try to pet it immediately (error #1)
  - Try to play with it (error #1)
- **Subsequent choices**: Each wrong decision leads you closer to the bad ending
- **Redemption paths**: Some mistakes can be corrected if you make better choices afterward

#### Folder Structure
```
/var/www/html/
├── start/
│   ├── index.html
│   ├── abrir_puerta.html
│   └── no_abrir_puerta.html
├── care/
│   ├── alimentar_primero.html
│   ├── acariciar_primero.html
│   ├── jugar_primero.html
│   ├── despues_alimentar.html
│   └── mascota_molesta.html
├── interaction/
│   ├── jugar_feliz.html
│   └── acariciar_con_cuidado.html
├── end/
│   ├── final_malo.html
│   ├── final_neutro.html
│   ├── final_neutro_dos.html
│   └── final_bueno.html
└── images/
    ├── Door.PNG
    └── ... (other images)
```

**Note**: Folder names are in English (start, care, interaction, end) but page content is in Spanish.

## How to Run the Game

#### Prerequisites
- NGINX web server installed
- WSL (Windows Subsystem for Linux) or a Unix terminal
- Basic terminal knowledge

#### Installation Steps

##### 1. Clone or Download the Repository
##### 2. Copy Files to NGINX Directory
```bash
sudo chown -R $USER:$USER /var/www/html

cp -r * /var/www/html/

ls -la /var/www/html/
```

##### 3. Start NGINX
```bash
sudo systemctl start nginx

sudo systemctl status nginx

sudo systemctl enable nginx
```

##### 4. Access the Game through your local host

## Important Notes About File Paths

#### Image Paths
All image references in HTML files use **relative paths**:
- From files in subfolders (start/, care/, etc.): `../images/image_name.PNG`
- Example: `<img src="../images/Door.PNG" alt="Door" width="400">`

#### Navigation Links
All navigation links between pages use **relative paths**:
- From `start/` to `care/`: `<a href="../care/alimentar_primero.html">Feed it</a>`
- From `care/` to `end/`: `<a href="../end/final_bueno.html">Good ending</a>`
- Within same folder: `<a href="abrir_puerta.html">Open door</a>`


### Gameplay Tips

1. **Read carefully** - The text provides hints about the creature's needs
2. **Think logically** - A hungry creature won't want to play or be touched
3. **Pay attention to warning signs** - Red eyes and raised scales mean danger
4. **There are multiple paths** - Not all mistakes lead to the bad ending immediately
5. **Explore different routes** - Try playing multiple times to discover all endings

### Technical Details

#### Technologies Used
- **HTML5**
- **NGINX**

#### HTML Elements Used
Each page includes:
- `<head>` with metadata and title
- `<header>` for page headers
- `<body>` for main content
- `<footer>` for credits
- At least one heading (`<h1>`, `<h2>`, `<h3>`)
- Paragraphs with `<p>`
- Images relevant to the content
- Text formatting (`<b>`, `<strong>`, `<em>`, `<small>`)
- Navigation links with `<a>` tags

### Development Notes

#### Design Choices
- The game uses **branching HTML paths** to simulate different outcomes
- Critical errors are tracked by leading users down specific HTML file paths
- Each ending is a separate HTML file with completely different content
- Now the game shows a better interface

### Credits

- **Code, Photography (the dogs), and Drawings**: Enya Gálvez - 24693
- **Other Pictures**: 
    - bird with hat: <a href="https://www.pinterest.com/meowywowie/">@meowywowie</a> from <a href="https://www.pinterest.com/pin/605804587419449992/">Pinterest</a>.
    - tiger eating meat: <a href="https://unsplash.com/es/@dinesh_d_kumar?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Dinesh Kumar</a> from <a href="https://unsplash.com/es/fotos/un-tigre-blanco-comiendo-un-trozo-de-carne-_cWptj938AQ?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>.
            </small></p>
- **Date**: February 10, 2026
- **Course**: Web Systems and Technologies
- **Institution**: Universidad del Valle de Guatemala
- **Instructor**: Marlon Fuentes


### Happy Gaming!

Enjoy your adventure as a Mythical Creature Guardian! Remember: every choice has consequences.

# Table of contents

* [Description](#description)
* [Installation](#installation)
* [Screenshots](#screenshots)

# Description

**Hypertube is a torrent-based Netflix-like website.**

It allows logged users to search for and watch films in streaming. The search box is directly connected to torrent websites (using their APIs) and, as soon as a user clicks "Play" on a film, the file is downloaded on the server and streamed on the web player at the same time. See [hypertube.fr.pdf](../master/hypertube.fr.pdf) for details.

This was a 19 Coding School web project. It was coded using MEAN stack (MongoDB, Express.js, Angular, Node.js) for 6 weeks in 2020 by Clio Brichaut (@cbrichau), Adam Ceciora (@adamceci) and Yassine Chahbar (@ychahbar19).

**Final grade: 110%** (points for implementing bonuses).

Peer evaluations:
> 115% _"Bon Netflix les gars ! Rien à dire, très bon projet ! A la revoyure !"_

> 109% _"Super top ! Très grosse motive de votre part de le faire en Angular ce qui vous a fait gagner un point bonus. Site intuitif simple d'utilisation , mieux que la plupart des sites streaming sur le marché !"_

> 109% _"Bravo la team, projet très propre et fonctionnel. L' UX/UI est sympa. On sent la maîtrise dans les technos choisies et une team très soudée malgré les difficultés rencontrées et ça, c'est beau ;). Bonne chance pour la suite"_

> 112% _"Vraiment bon boulot! En plus bravo pour le choix Angular!"_

> 109% _"Très bon boulot, très beau site."_

# Installation

> Working as of Feb 2023.

1. Clone the repo.

2. Create a free [MongoDB Atlas](https://www.mongodb.com/atlas/database) cluster and add its link to `Hypertube\back\config\database.js` at line 7: `mongoose.connect('mongodb+srv://USERNAME:PASSWORD@CLUSTER/test?retryWrites=true&w=majority'`.

2. Launch the backend by running:
   * `cd back`
   * `npm install`
   * `nodemon`
      * If you get the "os.tmpDir is not a function" error, go to `Hypertube\back\node_modules\torrent-stream\index.js` and add this at line 36: `os.tmpDir = os.tmpdir;` (just before `var TMP = fs.existsSync('/tmp') ? '/tmp' : os.tmpDir()`).
   * The backend should now be running on port 3000.

3. In another terminal, launch the frontend by running:
   * `cd front`
   * `npm install`
   * `ng serve`
      * If you get the "ng command is not found" error, install angular with `npm install -g @angular/cli@latest` then serve again.
   * The frontend should now be running on port 4200.

4. Open http://localhost:4200/ to view the app.

# Screenshots

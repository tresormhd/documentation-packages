# documentation-packages

Listes des packages :
* express
* ejs
* mongoose
* mongoose-relationship
* axiox

# Express 
- desciption

Express est une infrastructure d'applications Web Node.js minimaliste et flexible qui fournit un ensemble de fonctionnalités robuste pour les applications Web et mobiles. 
- instalation et utilisation 

        npm install express --save
Apres installation il faut require dans server.js

        var express = require('express')
        var app = express() 

        app.get('/', function (req, res) {
        res.send('Hello World')
        // ce code renvoie "Hello World" dans le naviguateur 
        })

        app.listen(3000)

# ejs

- description 

EJS est un langage de modélisation simple qui vous permet de générer un balisage HTML avec JavaScript. Aucune religion sur la façon d'organiser les choses. Aucune réinvention de l'itération et du flux de contrôle. C'est du simple JavaScript.

- installation 

        npm install ejs
 
- utillisation 

apres il faut configurer le view engine  

        app.set('views','./views');
        app.set('view engine','ejs')

          - les tags utilisés dans la page ejs 

            <%  %> Balise 'Scriptlet', pour le contrôle-flux, pas de sortie
            <%_  _%> ‘Balise de scriptlet d’espacement des blancs, supprime tous les espaces blancs
            <%= %> Affiche la valeur dans le modèle (HTML échappé)
            <%- -%>  Affiche la valeur non échappée dans le modèle
            <%# %> Balise de commentaire, pas d'exécution, pas de sortie
    
    
# mongoose 

- description 
    
Mongoose est un outil de modélisation d'objet MongoDB conçu pour fonctionner dans un environnement asynchrone comme nodejs .

- installation 
    
      npm install mongoose
   
- connexion a la base de donnée 
   
       const mongoose = require('mongoose');

      mongoose.connect('mongodb://localhost/nom_de_la_base_de_donnée', {
        useNewUrlParser: true,
        useUnifiedTopology: true
      });


- creer un schema 

          const Schema = mongoose.Schema;
        const ObjectId = Schema.ObjectId;

        const BlogPost = new Schema({
          author: ObjectId,
          title: String,
          body: String,
          date: Date
        });

- creer un modele 

      const MyModel = mongoose.model('ModelName', mySchema);  
  
voici le lien pour plus d'informations sur les requetes : https://mongoosejs.com/docs/ 
  
# mongoose-relationship

- description 

ce module permet de creer et gerer les relations entres les collections avec la DB mongodb plus facilement .
Il peut y avoir plusieurs type de relations : One-To-One, One-To-Many, or Many-To-Many


- installation

      npm install mongoose-relationship
   
- utilisation 

https://www.npmjs.com/package/mongoose-relationship

# axios 

- desciption 

axios est utilisé pour faire des requetes et travailler les resultats avec les promises 
- installation 

axios peut etre instaler de diferente maniere 

      avec npm : npm install axios`` 
      
      avec cdn : <script src="https://unpkg.com/axios/dist/axios.min.js"></script>  
- utilisation
    
https://www.npmjs.com/package/axios 
    

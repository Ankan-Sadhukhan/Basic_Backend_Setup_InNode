Setup guide 🚀

- do, npm install -> to install all packages, dependencies
- create .env file, mention PORT 
- create config.json file inside src/config/ --> put your database details there --> npx sequelize init
- to run, npm start

Database setup(MySQL) 🚀

- npx sequelize init -> Before this, delete model folder and config.json if exists The command creates config.json file & basic folder setup for db. we have already done it. put config.json in .gitignore file
- after saving your details in config.json,
- npx sequelize db:create (make sure you are inside src/ folder)

Creating Model(table)  🚀  * model - singular, table - plural
- npx sequelize model:generate --name City --attributes name:string, pin:integer  
*/ it will create new model, migrations folder. --> You can change properties /*
- npx sequelize db:migrate */ changes visible in MySQL server /*

Undo migrations 
- npx sequelize db:migrate:undo

Seeding data to table  🚀
- npx sequelize seed:generate --name <fileName, eg:add-cities>
*/ add data to this file(add-cities) /*
- npx sequelize db:seed --seed <fileName/eg:add-cities> 

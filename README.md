# first-project-recap

downloading step

1. express 2. mongoose 3.typescript dev defency hisbe download dite hobe 4.cors 5.dotenv

tsc initial korte hobe tsc -init (rootdir er modde thakbe ./src ar outdir er modde ./dist) erpor src folder banabo er modde app.ts ebong server.ts file banabo ar eta k run korar jonno package.json er modde build namok structure banabo jekhane thakbe tsc. Server.ts er modde sokol server er code rakhbo ar er modde mongoose ba ja connect kora lage eikhane korbo. eropor mongodb atlas er sathe connect korbo (https://www.mongodb.com/cloud/atlas/register) ei link e giye. ERPOR database access e giye notun user toiri korbo.mongodb+srv://admin-um2:X3DdQCGBl9nfOcrp@cluster0.kxul6c6.mongodb.net/(eikhane project er nam dibo)?retryWrites=true&w=majority. dotenv theke process korar jonno src er modde app namok folder banabo.er modde arekta folder banabo config.config er modde index.ts namok file banabo.index.ts er modde
import dotenv from "dotenv";
import path from "path";

dotenv.config({ path: path.join(process.cwd(), ".env") });

export default {
port: process.env.PORT,
database_url: process.env.DATABASE_URL,
};

egula dibo. server port ba onno sob gula code mongoose er main er vitore dukabo. ar sob gula code try catch er modde dukabo. app.ts er modde parser user korbo (
app.use(express.json());
app.use(cors());
)

eslint ar prettier download korar jonno step gula nite hobe
ei command ta dite hobe (npm install --save-dev typescript) ts config.json er set up kore ei command dite hobe (npm install eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev)
erpor eta dite hobe (npx eslint --init) erpor prosno gular ans dite hobe ekta prosno hobe emon ? What format do you want your config file to be in? er ans hobe json. rules add korar por root er modde .eslintignore ei file banate hobe. package .json er modde eta dite hobe
"lint": "eslint src --ignore-path .eslintignore --ext .ts",

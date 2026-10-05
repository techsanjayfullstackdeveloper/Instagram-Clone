created prisma accound using my google accout sanayraaz2 
login to prisma and created workspace
serached docs (NextJs) and install bellow packages 

# npm install prisma@prev tsx @types/pg --save-dev
# npm install @prisma/client@7 @prisma/adapter-pg dotenv pg

Once installed above packages, initialize Prisma in your project using bellow command

# npx prisma init --db --output ../app/generated/prisma

This will create:

# A prisma directory with a schema.prisma file.
# A prisma.config.ts file for configuring Prisma.
# A .env file containing a local DATABASE_URL at the project root.

The app/generated/prisma output directory for the generated Prisma Client will be created when you run prisma generate or prisma migrate dev in a later step.

Once we run "npx prisma init --db --output ../app/generated/prisma" then we need to authenticate using google emailId eg: "sanjayraaz2" 

create project with the name eg: Instagram-Clone





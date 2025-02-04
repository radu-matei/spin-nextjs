# A simple Next.js statically generated application, running on Spin

This is a template for building and statically exporting your
[Next.js 14](https://nextjs.org) application and running it on
[`Fermyon Spin`](https://developer.fermyon.com/spin).

## Using the template

First, you need to tell the Spin CLI where to get the template:

```console
$ spin templates install --git https://github.com/radu-matei/spin-nextjs
Copying remote template source
Installing template nextjs-frontend...
Installed 1 template
+--------------------------------------------------+
| Name              Description                    |
+==================================================+
| nextjs-frontend   Simple front-end using Next.js |
+--------------------------------------------------+
```

Then, you can either create a new application based on this template:

```console
$ spin new -t nextjs-frontend my-nextjs-app
# your new application has been created in the my-nextjs-app directory
```

Alternatively, you can add a new component based on this template to an existing
Spin application:

```console
# first, create a new Spin application
$ spin new -t http-empty my-spin-app --accept-defaults && cd my-spin-app
$ spin add -t nextjs-frontend --accept-defaults
```

## Building and running your application

Before you can build your Next.js application, make sure to run `npm install` in
the target directory. You are now ready to start building your front-end. Run
`npm run dev` and start editing your application. Alternatively, you can run
`spin build` and `spin up` to build and run your application.

## What can you do next?

Use another Spin template to build your serverless back-end and call it from
your newly-built front-end. For example:

```console
$ spin add -t http-ts api
# a new Spin component called `api` has now been created in your application
$ spin build && spin up
Available Routes:
  web: http://127.0.0.1:3000 (wildcard)
  api: http://127.0.0.1:3000/api (wildcard)
```

## Deploy your application to Fermyon Cloud

Using a free [Fermyon Cloud](https://cloud.fermyon.com) account, you can deploy
your serverless WebAssembly applications and get a public URL:

```console
$ spin deploy
# your application will now be available at a *.fermyon.app URL
```

## Credits

The Next.js template is based on the
[official Next.js template](https://nextjs.org/docs/api-reference/create-next-app).

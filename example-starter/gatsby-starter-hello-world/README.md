<!-- AUTO-GENERATED-CONTENT:START (STARTER) -->
<p align="center">
  <a href="https://www.gatsbyjs.org">
    <img alt="Gatsby" src="https://www.gatsbyjs.org/monogram.svg" width="60" />
  </a>
</p>
<h1 align="center">
  gatsby's hello-world starter
</h1>

starter를 이용 react 구조를 빠르게 만들어내는 gatsby.

- pages name을 활용 web page와 uri를 자동 생성.

_더 알아보기 [official and community-created starters](https://www.gatsbyjs.org/docs/gatsby-starters/)._

## 🚀 Quick start

1.  **Gatsby site 만들기**

    gatsby-cli와 hello-world starter을 활용하여 새로운 사이트를 만든다.

    ```shell
    # gatsby new [projectname] [stater]
    gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world
    ```

1.  **개발하기.**

    Navigate into your new site’s directory and start it up.

    ```shell
    cd hello-world
    gatsby develop
    ```

1.  **Open the source code and start editing!**

    Your site is now running at `http://localhost:8000`!

    _Note: You'll also see a second link: _`http://localhost:8000/___graphql`_. This is a tool you can use to experiment with querying your data. Learn more about using this tool in the [Gatsby tutorial](https://www.gatsbyjs.org/tutorial/part-five/#introducing-graphiql)._

    Open the `hello-world` directory in your code editor of choice and edit `src/pages/index.js`. Save your changes and the browser will update in real time!

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in a Gatsby project.

    .
    ├── node_modules
    ├── src
    ├── .gitignore
    ├── .prettierrc
    ├── gatsby-browser.js
    ├── gatsby-config.js
    ├── gatsby-node.js
    ├── gatsby-ssr.js
    ├── LICENSE
    ├── package-lock.json
    ├── package.json
    └── README.md

1.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

2.  **`/src`**: This directory will contain all of the code related to what you will see on the front-end of your site (what you see in the browser) such as your site header or a page template. `src` is a convention for “source code”.

3.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

4.  **`.prettierrc`**: This is a configuration file for [Prettier](https://prettier.io/). Prettier is a tool to help keep the formatting of your code consistent.

5.  **`gatsby-browser.js`**: This file is where Gatsby expects to find any usage of the [Gatsby browser APIs](https://www.gatsbyjs.org/docs/browser-apis/) (if any). These allow customization/extension of default Gatsby settings affecting the browser.

6.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. (Check out the [config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

7.  **`gatsby-node.js`**: This file is where Gatsby expects to find any usage of the [Gatsby Node APIs](https://www.gatsbyjs.org/docs/node-apis/) (if any). These allow customization/extension of default Gatsby settings affecting pieces of the site build process.

8.  **`gatsby-ssr.js`**: This file is where Gatsby expects to find any usage of the [Gatsby server-side rendering APIs](https://www.gatsbyjs.org/docs/ssr-apis/) (if any). These allow customization of default Gatsby settings affecting server-side rendering.

9.  **`LICENSE`**: Gatsby is licensed under the MIT license.

10. **`package-lock.json`** (See `package.json` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(You won’t change this file directly).**

11. **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

12. **`README.md`**: A text file containing useful reference information about your project.

## 🎓 Learning Gatsby

Looking for more guidance? Full documentation for Gatsby lives [on the website](https://www.gatsbyjs.org/). Here are some places to start:

- **For most developers, we recommend starting with our [in-depth tutorial for creating a site with Gatsby](https://www.gatsbyjs.org/tutorial/).** It starts with zero assumptions about your level of ability and walks through every step of the process.

- **To dive straight into code samples, head [to our documentation](https://www.gatsbyjs.org/docs/).** In particular, check out the _Guides_, _API Reference_, and _Advanced Tutorials_ sections in the sidebar.

## 💫 Deploy

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gatsbyjs/gatsby-starter-hello-world)

[![Deploy with ZEIT Now](https://zeit.co/button)](https://zeit.co/import/project?template=https://github.com/gatsbyjs/gatsby-starter-hello-world)

## styling

- lnline styles
- global css
- css modules
- styled-components
- bootstrap, tailwind, emotion etc

## graphql

- loading data into react components
- don`t give up
- use gatsby docs
- graphiql -- graphql integrated development environment(ide) / graphql sandbox
- http://localhost:8000/___graphql
- practice

1. **data(api`s, headless cms, json, markdown, sitemetadata)**

2. **graphql**

3. **graphiql ide**

4. **<staticquery> <pagequery>**

5. **components - page, title, heading**

## data

1. **local**

   _json , markdown, mdx_

2. **external**

   _headless cms - contentful, strapi_

# [`contentful`](https://app.contentful.com/)

A content platform is everything a CMS isn’t. Control all of your content from a single hub. Publish to any digital channel. Integrate anything with our industry-leading app framework. See ya, CMS.

Digital experiences. Powered by Contentful.
It’s more than content management — it’s a content platform powerful enough to create amazing digital experiences at scale.

```sh
npm install --save gatsby-source-contentful
```

```ts
// In your gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: `gatsby-source-contentful`,
      options: {
        spaceId: `your_space_id`,
        // Learn about environment variables: https://gatsby.dev/env-vars
        accessToken: process.env.CONTENTFUL_ACCESS_TOKEN,
      },
    },
  ],
}
```

[`Environment Variables`](https://www.gatsbyjs.org/docs/environment-variables/)

## GraphiQL

```ts
query MyQuery {
  allContentfulProduct {
    nodes {
      title
      slug
      price
      image {
        fluid {
          src
        }
      }
    }
  }
}
```

## templates

pages 안에 파일을 name에 맞추어 uri 자동생성하는것을 사용함과 별개로
product detail 과 같이 여러 page를 자동생성하는것에 무리가 있다.
이때 template을 사용.

```ts
// gatsby-node.js
const path = require("path")

// create pages dynamically
exports.createPages = async ({ graphql, actions }) => {
  const { createPage } = actions
  const result = await graphql(`
    query GetProducts {
      products: allContentfulProduct {
        nodes {
          slug
        }
      }
    }
  `)
  result.data.products.nodes.forEach(product => {
    createPage({
      path: `/products/${product.slug}`,
      component: path.resolve(`src/templates/product-template.js`),
      context: {
        slug: product.slug,
      },
    })
  })
}
```

## GraphiQL

```ts
query GetSingleProducts($slug:String) {
  product: contentfulProduct(slug: {eq: $slug}) {
    title
    price
    image {
      fixed {
        src
      }
    }
    info {
      info
    }
  }
}


// query variables
{
  "slug": "leather-sofa"
}
```

## styling

1. **inline styling**

```ts
<h1 style={{ color: "red", textTransform: "uppercase" }}>Hello from gatsby</h1>
```

2. **global css**

```ts
// layout.js
import "./layout.css"

// layout.css
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap");

body {
  font-family: "Roboto", sans-serif;
  background-color: teal;
}

h1 {
  color: blueviolet;
  text-transform: capitalize;
}

p {
  line-height: 2;
}
```

glabal css 사용할시 className을 일일히 만들어주어 control 해야하고,
app 단위가 커지면 className이 중복되는 경우 error가 발생할 가능성이 높아진다.

이를 해결하기 위해 2가지 방법이 있다. css파일을 module화 하여 정해진 단위로
나누어 적용할수도 있고 styled-component를 활용하여 className 관리를 자동화.

3. **css modules**

```ts
// blog.module.css
.page {
  background: greenyellow;
}

.page h1 {
  color: orange;
}

.text {
  text-transform: capitalize;
}

// blog.js
import styles from "../components/blog.module.css"


// products.module.css
.page {
  background: violet;
}

.page h1 {
  color: palevioletred;
}

.text {
  text-transform: uppercase;
}


// products.js
import styles from "../components/products.module.css"
```

4. **styled-components**
   plugin

```ts
// gatsby-config.js
module.exports = {
  /* Your site config here */
  plugins: [
    {
      resolve: `gatsby-plugin-styled-components`,
      options: {
        // Add any options here
      },
    },
  ],
}
```

## GraphiQL

View GraphiQL, an in-browser IDE, to explore your site's data and schema

http://localhost:8000/___graphql

- CTRL + SPACE : 검색 가능 목록 확인.
- CTRL + ENTER : 실행

## [`Gatsby Config API`](https://www.gatsbyjs.org/docs/gatsby-config/)

```ts
// gatsby-config.js

module.exports = {
  /* Your site config here */
  siteMetadata: {
    title: "Gatsby Tutorial",
    description: "some random description",
    author: "@wnalsgkr",
    data: ["item1", "item2"],
    person: { name: "peter", age: 32 },
  },
```

GraphiQL에서 설정한 siteMetadata를 확인해보자

```ts
query MyQuery {
  site{
    siteMetadata{
      title
      description
      data
      person{
        age
        name
      }
    }
  }
}
```

## data 활용

외부 data나 위에서 처럼 설정값 들을 손쉽게 사용할수있다.

GraphiQL에서 찾아본 설정값들을 Code Exporter 사용.

page query, staticquery hook, static query 등

react 내부구조에 따른 대응.

```ts
// staticquery hook form
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const ComponentName = () => {
  const data = useStaticQuery(graphql`
    {
      site {
        siteMetadata {
          title
          description
          data
          person {
            age
            name
          }
        }
      }
    }
  `)
  return <pre>{JSON.stringify(data, null, 4)}</pre>
}

export default ComponentName
```

가져온 data 확인

```ts
return (
  <div>
    <h2>title: {data.site.siteMetadata.title}</h2>
    <h2>name: {data.site.siteMetadata.person.name}</h2>
  </div>
)
```

return 안에서 data를 사용시에 가독성을 좋게 하기 위해

```ts
const getData = graphql`
  {
    site {
      siteMetadata {
        title
        description
        person {
          name
          age
        }
      }
    }
  }
`

const {
  site: {
    siteMetadata: {
      title,
      description,
      person: { name, age },
    },
  },
} = useStaticQuery(getData)

return (
  <div>
    <h2>title : {title}</h2>
    <h2>description : {description}</h2>
    <h2>name : {name}</h2>
    <h2>age : {age}</h2>
  </div>
)
```

siteMetadata을 info 바꿔 다룰수있다.

```ts
const getData = graphql`
  {
    site {
      info: siteMetadata {
        title
        description
        person {
          name
          age
        }
      }
    }
  }
`

const {
  site: {
    info: {
      title,
      description,
      person: { name, age },
    },
  },
} = useStaticQuery(getData)
```

## Static Query

```ts
//static query form
import React from "react"
import { StaticQuery, graphql } from "gatsby"

const ComponentName = () => (
  <StaticQuery
    query={graphql`
      {
        site {
          info: siteMetadata {
            title
            description
            person {
              name
              age
            }
            author
            data
          }
        }
      }
    `}
    render={data => <pre>{JSON.stringify(data, null, 4)}</pre>}
  ></StaticQuery>
)

export default ComponentName
```

```ts
render={data => <h4>{data.site.info.description}</h4>}
```

## page 안에서 props 활용

```ts
// pages > index.js
import { graphql } from "gatsby"

export const data = graphql`
  query {
    site {
      info: siteMetadata {
        title
        description
        person {
          name
          age
        }
        author
        data
      }
    }
  }
`

const examples = ({ data }) => {
  const {
    site: {
      info: { author },
    },
  } = data

  return <h5>author: {author}</h5>
}
```

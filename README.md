# website-members

The part of the website that shows the members of RDS

## Project Structure

We are using Next.js for this project. Next.js has a well defined directory structure that must be used to make sure the apps runs properly. Read more about Next.js [here](https://nextjs.org/learn/basics/create-nextjs-app?utm_source=next-site&utm_medium=homepage-cta&utm_campaign=next-website)

### Pages

In `Next.js`, a page is a React Component exported from a `.js`, `.jsx`, `.ts`, or `.tsx` file in the `pages` directory. Each page is associated with a route based on its file/directory name. Read more about `pages` [here](https://nextjs.org/docs/basic-features/pages). An example is given below -

#### Directory Structure

```
pages
|__ members
|   |__ [id]
|   |   |__ index.js
|   |
|   |__ index.js
|
|__ blogs
|   |__ index.js
|
|__ index.js
```

#### Routes Created by Next.js

```
/
/members
/members/[id]
/blogs
```

> Note: In `/members/[id]` the `[id]` part is dynamic it can be `1`, `2`, `a`, etc.

### Components

All the reusable components are created inside `/components` directory.

### `/components/pages`

In Next.js it is adviced that the files inside `/pages` directory should contain as minimal code as possible, that's why all the code for a given page is written inside `/components/pages` directory and imported in `/pages`. For Example -

```JavaScript
// Inside /components/pages/blogs/index.js
import React from "react";
const Blogs = () => {
  return <div>This is my first documentation, I am super scared.</div>
};

export default Blogs;


// Inside /pages/blogs/index.js
import React from "react";
import Blogs from "../../components/pages/blogs";

const BlogsPage = () => {
  return (
    <div>
      <Blogs/>
    </div>
  );
};

export default BlogsPage;

```

> Note: Do not create individual files in `/components` or `/pages`. Put every file in folders with appropiate names.

### Public

All the public assets like `icons`, `images` are stored inside public directory.
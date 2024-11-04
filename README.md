How to Start Development of a Web App Using a T3 Stack

Have you ever wanted to create a web app and have no idea where to start? If that's the case you can start your journey with this guide that will instruct you on how to get started developing your first web app using a toolbox that I've spent months selecting. 

Things to download before you start:
A code editor such as Visual Studio Code or Cursor
node.js


1.First navigate to your desktop and right click an open space. 

2. Make a new folder on your computer named whatever you want your project to be named. I’ll be naming mine “test” as shown in the image below.

![Test Folder Image](test%20folder.png)

3. Use your code editor, I recommend using Visual Studio for beginners. Open the folder we just made with your code editor, then open the terminal. You can do this by either using CTRL+Shift+P and searching for terminal, or by using the shortcut which is `+P

4. Run the this command to download the files and create a t3 stack
npm create t3-app@latest(If you don’t have node.js you’ll need to install it here https://nodejs.org/en )

4.5 Help for if you’re still having issues with installing node.js


If you’re still getting an error that the module is missing:
You need to Add C:\Program Files\nodejs to your PATH environment variable. To do this follow these steps:
Use the global Search Charm to search "Environment Variables"

![search charm](images/Screenshot%202024-11-04%20at%203.09.37%20PM.png)

Click "Edit system environment variables"
Click "Environment Variables" in the dialog.
In the "System Variables" box, search for Path and edit it to include C:\Program Files\nodejs. Make sure it is separated from any other paths by a ;.
You will have to restart any currently-opened command prompts before it will take effect.
After this go back and try step 4 again.


5. There are many different frameworks to use, for this tutorial we’ll use Next.js from https://ui.shadcn.com/docs/installation

To add shad/cn’s capabilities to our app we run
npx shadcn@latest init	(choose npm)
(You can use the -d flag for defaults i.e new-york, zinc and yes for the css variables.
ex: npx shadcn@latest init -d

![Framework Image](framwork.png)

You’ll then get a few options if you don’t want default options
These options are for styling your website and changing things like the theme or fonts. 

6. After that you can use components from the shad/cn website by going to the component section from the website and copying the command into your terminal. In the image below you can see the button component and the command to install it. 

![Component Image](component.png)

7. To add these components you can import them with "import { Button } from "~/components/ui/button";" and then call it in your code!
ex:import React from 'react';
import Button from '~/components/ui/Button';

const HomePage = () => {
  const handleClick = () => {
    console.log("Button clicked!");
  };

  return (
    <div>
      <h1>Welcome to My T3 Stack App</h1>
      <Button label="Click Me" onClick={handleClick} />
    </div>
  );
};

export default HomePage;
   

8. Now you can edit files and run your app on your local host by running ‘npm run dev’ and in your terminal and then going to http://localhost:3000

I hope this tutorial was helpful for anyone trying to get into web development!

 


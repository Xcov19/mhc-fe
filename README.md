# mhc-fe
## My health connect frontend repository with design studio and frontend source code

## How to integrate figma, figma token to this repository

Design tokens are the visual design atoms of the design system — specifically, they are named entities that store visual design attributes, we can say they are variables that can be given a value.

Design tokens can be attributes such as: color, font, font size, spacing, border thickness, opacity, radius, shadow.

A good example of thinking about its application in the context of a project is to look at theme management, where we can have a color guide for light mode, or dark mode, or even themes for seasonal periods such as Black friday, Christmas, for example.

When we have pages in light mode, we use colors for fonts, colors for background, colors for buttons, colors for SVG illustrations other than dark mode, this is because we need to guarantee the contrast and good usability and accessibility of this product, be it a web or mobile.

And when we talk about a project with many pages, let's say in passing that without a well-elaborated design system, and with constant maintenance, it will be quite tiring to make changes and future updates with a certain speed.

Implementing design tokens in a project gives it scalability, allowing that by replacing the value of a few tokens, you have an entire project already re-purposed and ready for use, without much intervention from a developer.

Let's see an example:

<img width="435" alt="image" src="https://user-images.githubusercontent.com/104807903/200140203-c7681c8a-eeff-4691-a7dd-2d74886b83df.png">

When we look at the situation above, we understand that when we have a darker background, it was necessary for the designer to also change the color of the button, and also the color of the label of this button so that we could have a good reading of it.

Now think that without the use of tokens, it should be necessary for the developer to replace these values in hexadecimal, for example:

Background: #FFFFFF -> #3D3D3D<br>
Fill Button: #3D3D3D -> #EEEEEE<br>
Color Text: #FFFFFF -> #5C5C5C<br>

That is, when the designer needs to establish some change, the developer is impacted by it in a substantial way, where he would now need to review his code in search of correcting these colors throughout the project.

Now, when using Design tokens we can have the following hypothesis

Background: $background.color<br>
Fill Button: $buttom.color<br>
ColorText: $text.color<br>

The developer sees the colors as variables, and it is the design who establishes the values that this variable will receive, the design in this way has the autonomy to define changes to the colors, and the developer no longer needs to carry out a review of the project, because every it will get the changes defined by expecting the attribute with a variable value

Figma is an amazing tool, without a doubt, but without the help of third-party software, it still doesn't have the ability to build all these tokens on its own. So, for that, we use a plugin, Figma tokens.

Figma tokens allows us to create the themes that will be used in the projects, as well as the tokens that will be used in each of them, and the plugin takes care of building a JSON object that can be consumed by the project developers.

To use it just install it through the link (https://www.figma.com/community/plugin/843461159747178978/Figma-Tokens)

Today we also have all the documentation that is maintained by the Figma Tokens team, where we can be consulting the future updates of the plugin and how to use it (https://docs.figmatokens.com/)

### How to integrate figma, figma token to this repository

To use project tokens, you will first need to have your figma tokens plugin installed, and then have an account on your github so that you can later consume existing tokens in your commits with token updates.

<ol>
<li>Login to your github account</li>
<li>Go to the user's photo located in the upper right corner of the screen and click to display the options</li>
<li>click settings</li>
<li>On the left side you will have a long list, go to the last option "developer settings" and click on it</li>
<li>Again in the left column, in Personal access token, choose the option: "Tokens (Classic)"</li>
<li>Click on Generate New Token and choose the option "Generate New Token (Classic)"</li>
<li>Now we will fill this form with the following information
<ul>
<li>in Note: give a name for the token that will be generated, We suggest "My Health Connect Token" without quotes</li>
<li>on Expiration: choose the option "no expiration"</li>
<li>In Select Scopes: but only the first option "repo" and the sets within it will also be marked automatically</li>
<li>At the end of the form, click on the green "Generate token" button</li>
<li>now reserve the generated token, as we will use it later inside Figma tokens</li>
</ul></li>
<li>Run the Figma Tokens plugin in figma on the My heath Connect project page</li>
<li>Go to the settings menu, located at the top of the plugin screen</li>
<li>Choose Github option for token storage</li>
<li>Then click on the add new credential button</li>
<li>Now we will fill this form with the following information
<ul>
<li>Name: Give this form a name of your choice, we recommend "My Health Connect Tokens", without the quotes</li>
<li>Personal Access Token: In personal access token, we will paste the previously generated access token on Github</li>
<li>Repository: Now just enter in the repository field "Xcov19/mhc-fe" without the quotes (here we are saying where the file with the tokens will be hosted)</li>
<li>Branch: Enter "develop" without the quotes (this is the branch that will be used so we can update the tokens)</li>
<li>File Path: Now you will enter the filename on Github "theme.json" without quotes</li>
<li>click save</li>
<li>make your first commit</li>
</ul></li>
</ol>


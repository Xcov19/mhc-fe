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

Background: #FFFFFF -> #3D3D3D
Fill Button: #3D3D3D -> #EEEEEE
Color Text: #FFFFFF -> #5C5C5C

That is, when the designer needs to establish some change, the developer is impacted by it in a substantial way, where he would now need to review his code in search of correcting these colors throughout the project.

Now, when using Design tokens we can have the following hypothesis

Background: $background.color
Fill Button: $buttom.color
ColorText: $text.color

The developer sees the colors as variables, and it is the design who establishes the values that this variable will receive, the design in this way has the autonomy to define changes to the colors, and the developer no longer needs to carry out a review of the project, because every it will get the changes defined by expecting the attribute with a variable value

Figma is an amazing tool, without a doubt, but without the help of third-party software, it still doesn't have the ability to build all these tokens on its own. So, for that, we use a plugin, Figma tokens.

Figma tokens allows us to create the themes that will be used in the projects, as well as the tokens that will be used in each of them, and the plugin takes care of building a JSON object that can be consumed by the project developers.

To use it just install it through the link (https://www.figma.com/community/plugin/843461159747178978/Figma-Tokens)

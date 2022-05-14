# Bar loader animation using only HTML and CSS.

## To make Custom Theme Loader

If your website has a Theme and you want to give the theme color in "Loader" then following these steps:

  (1) Remove the {filter: hue-rotate()} function in loader Animation.
  
  (2) Set the theme color as a "Backgorund-color" in only Animation and your code looking like this:
  
        @keyframes barLoader { 
            0%, 50%, 100% { 
                background: theme-color; 
            }
         0%, 100% { 
             transform: scaleY(0.1); 
             }
          50% { 
              transform: scaleY(1);
               } 
        }

    *Note: Don't set any "Backgorund-color" in bar(html-class) like this:
        
           .bar { 
                 width: 2rem; height: 10rem;

                 ❌❌❌❌ Don't do this ❌❌❌❌
                 backgound-color: theme-color;   /* This will change your loader Animation starting state */
                 ❌❌❌❌ ⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆ ❌❌❌❌

                 animation: barLoader 1.2s linear infinite;
                 display: inline-block;
                 transform-origin: bottom;
                 animation-delay: calc(0.1s * var(--i));
           }
## ❤ Thanks for reading ❤

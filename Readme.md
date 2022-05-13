**Please read this if you want to change something in Loader animation control**

1. If your website has a Theme and you want to give the theme color in "Loader" then following these steps:
    (a)Remove the {filter: hue-rotate()} function in loader Animation
    (b)Set the theme color as a "Backgorund-color" in only Animation and your code looking like this:
        @keyframes barLoader {
            0%,
            50%,
            100% {
                background: **theme-color**;
            }
            0%,
            100% {
                transform: scaleY(0.1);
            }
            50% {
                transform: scaleY(1);
            }
        }
        *Note: Don't set any "Backgorund-color" in bar(html-class) like this:
            .bar {
                width: 2rem;
                height: 10rem;

                ** Don't do like this **
                backgound-color: theme-color;   /* This will change your loader starting Animation */

                animation: barLoader 1.2s linear infinite;
                display: inline-block;
                transform-origin: bottom;
                animation-delay: calc(0.1s * var(--i));
            }

        (c) You can change "width" or "height" of bars according to your satisfaction.

__Thanks for reading this. I hope now you don't make any mistake. Happy Coding__
               
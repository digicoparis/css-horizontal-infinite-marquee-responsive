# css-horizontal-infinite-marquee-responsive

A perfect responsive horizontal infinite marquee that don't use Javascript. Works with text and images (aka logo row).

Instructions:

1. Set marquee class as required on your HTML elements:

.marquee {
grid-column-gap: 3rem;
grid-row-gap: 3rem;
display: flex;
overflow: hidden;
}

Both gaps should be set according to duration in your keyframe animation (animation.css):

@keyframes scroll {
from {
transform: translateX(0);
}
to {
transform: translateX(calc(-100% - 3rem));
}
}

Notice translateX - 3rem : same spacing as gap defined above.

2. Your need to use the following structure, for instance:
   marquee - marquee-content - contents - exactly same duplicate content

3. If you add reverse class on HTML element, it will reverse sliding order

Some fixes for mobile if you are having issues/flickering

1. Add -webkit-transform: translateZ(0); to your image elements
2. Set loading to eager on all images
3. Set width to 100%

Full details on https://www.youtube.com/watch?v=ZMCNin2VjxU

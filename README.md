The Internet Folks Assignment 2 - Samyak Jain

Bugs -

1. Fixed bug at FormSelect - Overlapping and mixing with the below FormSelect

```
import React, { useEffect, useRef, useState } from "react";
import { menuPortalCSS } from "react-select/dist/declarations/src/components/Menu";

const menuPortalTargetRef = useRef(null);
const [bodyElement, setBodyElement] = useState<HTMLElement | null>(null);

useEffect(() => {
    setBodyElement(document.body);
}, []);

menuPortalTarget={bodyElement}

<!-- In options add the following -->
color: "black"

<!-- Below options add the following -->
menu: (base) => ({
...base,
position: "absolute",
zIndex: "999 !important",
top: "-30px",
}),

```

2. Fixed bug at FormSelect - Added white color to the selected option of FormSelect

singleValue: (base) => ({
...base,
color: "white"
}),

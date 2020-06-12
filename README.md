# use-media-query
Custom hook to useMediaQuery in React components

## Source code
```
import { useState } from "react";

export const useMediaQuery = (query: string) => {
	const mediaQuery = window.matchMedia(query);
	const [matches, setMatches] = useState(mediaQuery.matches);
	mediaQuery.onchange = (e) => {
		setMatches(e.matches);
	};
	return matches;
};
```

## Example usage

const isMobile = useMediaQuery("(max-width: 450px)");

# About Me
```ts
interface Human {
  name: string;
  interests: string[];
  profession?: Profession<any>;
  favoriteBook?: { title: string; author: string };
}

interface Profession<T> { title: string; description: string; yearsExperience: number; }

interface Developer extends Profession<Developer> {
  languages: string[];
  frameworks: string[];
  tools: string[];
}

type Employment = Profession<any> | undefined;

// 🤨🔎 About Me 

const whoIAm = ( { whatIDo }: { whatIDo: Employment } ): Human => {
  return {
    name: 'Adam G. Emerson',
    profession: whatIDo,
    interests: ['Human Computer Interaction', 'Natural Language Processing', 'Crossword Puzzles'],
    favoriteBook: {title: 'Cats Cradle', author: 'Kurt Vonnegut Jr.'},
  }
}

const whatIDo: Developer = {
  title: 'Software Engineer',
  description: '✨🧙🏻 Making internet dreams come true. 👨🏻‍💻✨',
  yearsExperience: 3,
  languages: ['TypeScript', 'JavaScript', 'Python'],
  frameworks: ['React', 'Next.js', 'Astro', 'Express', 'Flask'],
  tools: ['WebStorm', 'Git', 'Docker', 'AWS'],
}

const adamGEmerson = whoIAm({whatIDo});
console.log(adamGEmerson);

```

# Some Stats
[![Adam G. Emerson's Github Stats](https://github-readme-stats.vercel.app/api?username=adamgemerson)](https://github.com/adamgemerson/github-readme-stats)

### Hi there 👋

<!--
**Alumin112/Alumin112** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

```rs
use std::collections::HashMap;

struct Programmer<'a> {
    braincells: u32,
    loves_rust: bool,
    likes_python: bool,
    known_languages: Vec<String>,
    extra_stuff: HashMap<&'a str, bool>,
}

impl<'a> Programmer<'a> {
    fn new(
        braincells: u32,
        loves_rust: bool,
        likes_python: bool,
        known_languages: Vec<String>,
        extra_stuff: HashMap<&'a str, bool>,
    ) -> Self {
        Self {
            braincells,
            loves_rust,
            likes_python,
            known_languages,
            extra_stuff,
        }
    }
}

fn main() {
    let mut bunch_of_cells = Programmer::new(
        42,
        true,
        true,
        vec!["C".to_owned(), "Python".to_owned(), "Rust".to_owned()],
        HashMap::new(),
    );

    bunch_of_cells
        .extra_stuff
        .insert("hates when teacher gives ton of homework", true);
    bunch_of_cells.extra_stuff.insert("is 14", true);
    bunch_of_cells.extra_stuff.insert("likes coding", true);
    bunch_of_cells
        .extra_stuff
        .insert("uses internet explorer", false);
}
```

## Welcome to GitHub Pages

## Fish
### Package Manager
https://github.com/jorgebucaran/fisher
### Bash support for Fish
https://github.com/edc/bass

## TypeScript Compiler 
### Setup
Note to self: Could run into future issue due to specifying node version

If your shell can not find the tsc command, the node /bin folders needs to be added to the path:
#### Bash
Add `export PATH="$PATH:"/usr/local/Cellar/node/14.4.0/bin/"";` to `~/.bash_profile`
#### Fish
`set -Ua fish_user_paths /usr/local/Cellar/node/14.4.0/bin/`

### NVM with Fish
Add the following to `~/.config/fish/functions/nvm.fish`
```bash
function nvm
    bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
end
```

### Environment Variables

#### Setup
An observable containing the env data

```markdown
class ClothingItem: ObservableObject {
    @Published var name: String = "croppedt"
}
```
#### Access
```Markdown
@EnvironmentObject var clothingItem: ClothingItem
```

### Binding
You can use @Binding / @State to set state in another struct, however it (struct with binding) must be intiailized where @State is accessible

### Specific corners rounded

```markdown
extension View {
    func cornerRadius(_ radius: CGFloat, corners: UIRectCorner) -> some View {
        clipShape( RoundedCorner(radius: radius, corners: corners) )
    }
}

struct RoundedCorner: Shape {

    var radius: CGFloat = .infinity
    var corners: UIRectCorner = .allCorners

    func path(in rect: CGRect) -> Path {
        let path = UIBezierPath(roundedRect: rect, byRoundingCorners: corners, cornerRadii: CGSize(width: radius, height: radius))
        return Path(path.cgPath)
    }
}

```
### Foundation

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
extension View {
    func cornerRadius(_ radius: CGFloat, corners: UIRectCorner) -> some View {
        clipShape( RoundedCorner(radius: radius, corners: corners) )
    }
}

struct RoundedCorner: Shape {

    var radius: CGFloat = .infinity
    var corners: UIRectCorner = .allCorners

    func path(in rect: CGRect) -> Path {
        let path = UIBezierPath(roundedRect: rect, byRoundingCorners: corners, cornerRadii: CGSize(width: radius, height: radius))
        return Path(path.cgPath)
    }
}

```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/thimbletech/thimbletech.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

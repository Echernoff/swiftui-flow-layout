# SwiftUIFlowLayout

A **Flow Layout** is a container that orders its views sequentially, breaking into a new "line" according to the available width of the screen. You can compare it to a left-aligned block of text, where every word is a `View`. A common use for this layout is to create a tag cloud.

The end result looks like this:

![in action](https://swiftuirecipes.com/user/pages/01.blog/flow-layout-in-swiftui/Screenshot%202020-11-20%20at%2010.54.37.png)

* The layout algorithm behaves differently if your FlowLayout is nested in a `VStack` or a scrollable parent, such as `ScrollView` or a `List`. Therefore, there's the **Mode enum and mode property**.

### Recipe

Check out [this recipe](https://swiftuirecipes.com/blog/flow-layout-in-swiftui) for in-depth description of the component and its code. Check out [SwiftUIRecipes.com](https://swiftuirecipes.com) for more **SwiftUI recipes**!

### Sample usage

```swift
struct FlowLayout_Previews: PreviewProvider {
  static var previews: some View {
    FlowLayoutView(mode: .scrollable,
                               binding: .constant(5),
                               items: ["Some long item here", "And then some longer one",
                                          "Short", "Items", "Here", "And", "A", "Few", "More", 
                                          "And then a very very very long one"]) {
      Text($0)
        .font(.system(size: 12))
        .foregroundColor(.black)
        .padding()
        .background(RoundedRectangle(cornerRadius: 4)
                               .border(Color.gray)
                               .foregroundColor(Color.gray))
    }.padding()
  }
}
```

### Installation

This component is distrubuted as a **Swift package**. 


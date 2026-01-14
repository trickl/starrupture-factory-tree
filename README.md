# Starrupture Construction Tree

This repository contains a mermaid diagram showing the construction tree and resource dependencies for building items in Starrupture.

## Construction Flow Diagram

The following diagram shows the resources and dependencies required to construct various items in Starrupture. Each node represents a resource or craftable item, and the arrows indicate what materials are needed to create each item.

```mermaid
graph TD
    %% Example construction tree - Update this with actual Starrupture data
    
    %% Raw Resources
    Iron[Iron Ore]
    Coal[Coal]
    Wood[Wood]
    Stone[Stone]
    
    %% Processed Materials
    IronBar[Iron Bar]
    Steel[Steel]
    Plank[Wooden Plank]
    Brick[Stone Brick]
    
    %% Components
    Gear[Gear]
    Circuit[Circuit Board]
    Frame[Metal Frame]
    
    %% Final Products
    Machine[Machine Tool]
    Structure[Structure Component]
    
    %% Dependencies
    Iron --> IronBar
    Coal --> IronBar
    IronBar --> Steel
    Coal --> Steel
    
    Wood --> Plank
    Stone --> Brick
    
    IronBar --> Gear
    Steel --> Frame
    IronBar --> Circuit
    
    Gear --> Machine
    Circuit --> Machine
    Frame --> Machine
    
    Steel --> Structure
    Brick --> Structure
    Frame --> Structure
    
    %% Style definitions
    classDef resource fill:#8B4513,stroke:#333,stroke-width:2px,color:#fff
    classDef processed fill:#4682B4,stroke:#333,stroke-width:2px,color:#fff
    classDef component fill:#9370DB,stroke:#333,stroke-width:2px,color:#fff
    classDef final fill:#228B22,stroke:#333,stroke-width:2px,color:#fff
    
    class Iron,Coal,Wood,Stone resource
    class IronBar,Steel,Plank,Brick processed
    class Gear,Circuit,Frame component
    class Machine,Structure final
```

## How to Update

To update this diagram with the correct Starrupture construction tree:

1. Edit the README.md file
2. Update the mermaid diagram within the \`\`\`mermaid code block
3. Add/remove nodes to represent actual in-game items and resources
4. Update the arrows (-->) to show the correct crafting dependencies
5. Adjust the style classes if needed to categorize different types of items

## Mermaid Syntax Reference

- `NodeName[Display Text]` - Creates a node with a label
- `A --> B` - Creates an arrow from A to B (A is required to build B)
- `A --> B --> C` - Chain multiple dependencies
- `%% Comment` - Add comments in the diagram
- Style nodes using `classDef` and `class` declarations

## Contributing

Feel free to improve the diagram or suggest additions. This is a community resource under CC0 1.0 Universal license.

## License

This work is marked with CC0 1.0 Universal. See the [LICENSE](LICENSE) file for details.

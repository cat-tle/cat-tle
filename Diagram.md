
```mermaid
---
Earth Example
---
classDiagram
    class Earth{
        +isHabitable()
        +int humanPop
    }
    class Land{
        +int numTrees
        +continents(amount)
    }
    class Ocean{
        +isBlue()
        +int numFish
    }
    class Sky{
        +hasClouds()
        +containsBirds()
    }
    class SpaceShips{
        +isSpaceAge()
        +onEarth(amount)
    }
    class humanShips{
        +numPeople(amount)
        +inOrbit()
    }
    class alienShips{
        +numAliens(amount)
        +int numPeople_kidnapped
    }

    Earth <|-- Sky
    Earth <|-- Ocean
    Earth <|-- Land
    SpaceShips <|-- humanShips
    SpaceShips <|-- alienShips
    Space <|-- Earth
    Space <|-- SpaceShips
    ```

##### Every entity is contained in space, Space ships and Earth. 
##### Alien and Human ships are both types of space ships and those they are both classed under SpaceShips.
##### However they are not on Earth thus do not fit under that class.
##### Land, Sky, and Ocean are all on earth. 
##### It's easier to class them under earth, so if we needed to edit earth as a whole, we wouldnt have to change every little thing that belongs to earth.
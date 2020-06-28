A simple game to learn Spanish words

## Solution and flow
I used MVVM design pattern. All of the game logic (i.e. success or failure feedback) and data loading is implemented in manager. GameViewModel can be access immutable livedatas defined in manager and exposes it to View (GameFragment). 

## Library and Solutions:
- **Koin** dependency injection
- **Coroutines** async data loading
- **MVVM** main app architecture (using AAC: ViewModel and LiveData)

## Time Allocation
I have spent about **8 hours and 45 minutes** to complete this project. (about **1 hour** is due to some **Gradle problems** with VPN at Iran)

- 1:00 hours to think and make decision about app architecture and logics (blue print for game logic)
- 1:45 hours to develop app structure (adding activity, fragments, GameManager interface and other classes for handling LiveData events and Gradle syncing problems:)
- 3:00 hours to implement ui (Custom CurveButton, GameFragment, WinnerDetailsFragment)
- 3:00 hours to implement game logic and handling ui updating with observer pattern and bug fixing

## Decisions
I decide to use MVVM design pattern for writing tests easily, but due to the time limit i was unable to complete test tasks. I did't use Repository pattern due to time limitation(it was better to have singltone repository that is responsible for data loading and communication with GameManager, if we have singleton repository there is no need for passing arguments to WinnerDetailsFragment and also testability will be improved). 

## Next Step?
There are the features which I would implement if I had enough time:

- Animation and UI improvements (i.e. text property for CurveButton in such a way the corresponding player could be easily read his/her name (drawing text in a curve path))
- Compliting test tasks
- Handling SavedInstanceState
- Game Settings (i.e. Players count, Theme, Difficultly level(game speed))

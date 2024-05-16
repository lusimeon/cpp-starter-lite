# CPP-starter-light

> Forked from https://github.com/TheLartians/MiniCppStarter and adapted to my specific needs.

## Features

- Separation of library and executable code
- Reproducible dependency management via [CPM.cmake](https://github.com/TheLartians/CPM.cmake)

## Usage

### Adjust the template to your needs

- Replace all occurrences of "App" in the relevant CMakeLists.txt with the name of your project
- Replace the source files with your own
- Happy coding!

### Build and run the standalone target

Use the following command to build and run the executable target.

```bash
cmake -S. -Bbuild && cmake --build build && ./build/App
./build/App --help
```

## FAQ

> I want something more sophisticated with test, format and CI.

Perhaps the [CppStarter](https://github.com/lusimeon/cpp-starter) is something for you!
# C/C++

* Weird debug output makes the program look like it's wrong, but indeed,
  the output routines are wrong (e.g. printing an `int *p;` as
  `print("%p\n", &p);`)
* `std::unique_ptr<T>` if that `class T` (e.g. `QWidget`) is owned by a
  parent that will delete it

# bash

* Have a function in a read-while-loop which also calls read - this can
  corrupt the for loop's read call, e.g. end the for loop unexpected

# git

* Making backups without care
  ```
  git pull origin master # I did not want to merge anything
  git add .
  cp -R git git_bak # but git_bak was not empty, so the result in git_bak was trash
  ```
* Pull from both origin and upstream => tons of merge conflicts



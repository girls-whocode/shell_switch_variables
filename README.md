# Variable Switcher #

## Instructions ##

At the beginning of your script include the variable.sh file
```source ./path/variable.sh```

## Usage ##

#### Keywords: ####
* "vs-next" will get the next value from options
* "vs-previous" will get the previous value from options
* "vs-ramdom" will generate a random value from options
* "vs-off" will unset the variable
* "vs-first" will get the first option from options
* "vs-last" will get the last option from options
* "vs-toggle" will switch between 2 arguments from the options
* or any value in your options list.

#### Example:

```
options=(
	"Number 1"
	"Number 2"
	"Number 3"
	"Number 4"
	"Number 5"
	"Number 6"
)

varswitch options[@] "MyVar" "Number 3" "Number 5"		# Your variable will now be Number 5
varswitch options[@] "MyVar" "Number 3" "vs-first"		# Your variable will now be Number 1
varswitch options[@] "MyVar" "Number 3" "vs-last"		# Your variable will now be Number 6
varswitch options[@] "MyVar" "Number 3" "vs-next"		# Your variable will now be Number 4
varswitch options[@] "MyVar" "Number 3" "vs-previous"		# Your variable will now be Number 2
varswitch options[@] "MyVar" "Number 3" "vs-random"		# Your variable will be a random value from your option list
varswitch options[@] "MyVar" "Number 3" "vs-off"		# The variable will be unset
```

Here is a toggle example:

```
options=(
	"enable"
	"disable"
)

varswitch options[@] "ToggleMyVar" "enable" "toggle"	# Your variable will now be disable
varswitch options[@] "ToggleMyVar" "disable" "toggle"	# Your variable will now be enable
```

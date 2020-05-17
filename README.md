# keep

It helps user to create backup easily.

## Install

```sh
git clone https://github.com/soni-vikas/keep.git
cd keep
sudo sh install.sh
```

## Usage

```
usage: keep [-s| --source] source [-d| --destination] [-t| --suffix] [--no-suffix] [-h]

```

## Flags

```
        -s, --source                Name of the source file or directory.
        -d, --destination           Default destination directory: '$HOME' - home directory.
        -t, --suffix                Provided suffix will get appended in source file/dir name.
                                    A copy of same will be save to destination.
                                    Example:
                                        keep file.txt -t vikas
                                         ->  keeping backup at:  HOME-DIR/.keep/file.txt_abc
        --no-suffix                 Keep the file-name as source file-same. Ignore [-t| --suffix]
        -h, --help                  Print help usage.
```

## Examples:
```sh

# create a test file
$ echo "this is a test file.txt" | cat > ~/file.txt

# Example: easy backup
$ keep ~/file.txt

... keeping backup at: /Users/vikas/.keep/file.txt_sun_may_17_15_05_52_ist_2020



# Example: easy backup, do not modify file-name
$ keep ~/file.txt --no-suffix

... keeping backup at: /Users/vikas/.keep/file.txt



# Example: Use of all flags
$ keep -s ~/file.txt -d ~/destination -t backup

... keeping backup at: /Users/vikas/destination/file.txt_backup

``` 

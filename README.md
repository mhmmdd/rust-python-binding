Download and install Python on Windows\
https://www.python.org/ftp/python/3.7.5/python-3.7.5-amd64.exe \
`$ python --version`\
_Python 3.7.5_

`$ cargo --version`\
_cargo 1.44.1 (88ba85757 2020-06-11)_

`$ rustc --version`
_rustc 1.44.1 (c7087fe00 2020-06-17)_

`$ rustup --version`\
_rustup 1.22.1 (b01adbbc3 2020-07-08)_

## Build Rust project mylib
`$ cargo build --release`

It would be .so on Linux or .dll on Windows\
`$ cp target/release/mylib.dll ./mylib.pyd`

### Raspberry Pi build
`$ python3 --version`\
_Python 3.7.3_\
`$ which python3`\
_/usr/bin/python3_\
`$ PYTHON_SYS_EXECUTABLE="/usr/bin/python3" cargo build --release`\
`$ cp target/release/libmylib.so ./mylib.so`


## Test on Python
`$ python`
```
Python 3.7.5 (tags/v3.7.5:5c02a39a0b, Oct 15 2019, 00:11:34) [MSC v.1916 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import mylib
>>> mylib.get_result('Hi') 
'Rust says: Hi' 
```
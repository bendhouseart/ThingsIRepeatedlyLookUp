# Matlab commonly used commands

## Adding items to path

### Addpath

only adds `.m` files to matlab path
usage:

```
mkdir('matlab/myfiles')   
addpath('matlab/myfiles')  
savepath matlab/myfiles/pathdef.m
```

[matlab\_documentation\_link](https://www.mathworks.com/help/matlab/ref/addpath.html)

### Adding None Matlab binary/folder to path

```
PATH = getenv('PATH');
setenv('PATH', [PATH ':/usr/local/desiredpath']);
unix('commandofinterest')
```

see -> [Executing unix commands set in PATH in matlab does not work with unix command](https://www.mathworks.com/matlabcentral/answers/27762-executing-unix-commands-set-in-path-in-matlab-does-not-work-with-unix-command)

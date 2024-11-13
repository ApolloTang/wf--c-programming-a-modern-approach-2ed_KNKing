# Setup jupyter for c



## Work with c in jupyter with jupyter-c-kernel

To work with c in jupyter install [jupyter-c-kernel](https://github.com/brendan-rius/jupyter-c-kernel) with pipenv: 

```
PIPENV_VENV_IN_PROJECT=1
pipenv install jupyter
pipenv install jupyter-c-kernel
pipenv run jupyter lab
```
**See example provided [here](./w-c-kernel/index.ipynb)**


## Work with c in Jupyter without the jupyter-c-kernel

Ref: [How to Code in C with a Jupyter Notebook - YouTube](https://www.youtube.com/watch?v=cWdU9unrlm0)

You can work with c in Jupyter without the jupyter-c-kernel by using the Ipython's magic commands `%%file` and `%%bash.` The `%%file` command allows you to edit a file, and the `%%bash` command lets you access the c-compiler installed on your computer in the bash shell. 

**See example provided [here](./w-no-c-kernel/index.ipynb)**

In the example I linked to, the c-compiler generates an executed file `main` can be ignored by git. Since the executable is extension less, the following has been added to the `.gitignore` in the root of this repository:
```
*
!/**/
!*.*
```
Note that the above should be placed at the beginning of the `.gitignore` file. (Ref: [git-ignore the extension-less file](https://stackoverflow.com/questions/19023550/how-do-i-add-files-without-dots-in-them-all-extension-less-files-to-the-gitign) (`c_program`, the executable))

In addition to the executable, the compiler also generates a [`.dSYM` folder](https://stackoverflow.com/questions/3656391/whats-the-dsym-and-how-to-use-it-ios-sdk)
which I am not sure what to do with, I'll ignore it for now by adding:

```
*.dSYM
```
to the `.gitignore`

To read: https://stackoverflow.com/questions/8237645/how-to-add-linux-executable-files-to-gitignore
add<br>
.container { width:100% !important}<br>
to the end of<br>
/usr/lib/python3/dist-packages/notebook/static/custom/custom.css

add<br>
c = get_config()<br>
c.InteractiveShellApp.matplotlib = 'notebook'<br>
c.InteractiveShellApp.extensions = ['sympy.interactive.ipythonprinting']<br>
to<br>
/etc/ipython/ipython_kernel_config.py<br>
reference https://ipython.readthedocs.io/en/stable/config/options/kernel.html and https://jupyterhub.readthedocs.io/en/stable/reference/config-user-env.html and https://ipython.readthedocs.io/en/stable/config/extensions/index.html and ipython3 --help and /usr/lib/python3/dist-packages/sympy/interactive/ipythonprinting.py and https://nbviewer.jupyter.org/github/ipython/ipython/blob/master/examples/IPython%20Kernel/Rich%20Output.ipynb

sudo -H pip3 install -t /usr/lib/python3/dist-packages xgboost<br>
when uninstall it said that xgboost not install and also download scipy and numpy

jupyter 3d visualization<br>
https://github.com/OpenDreamKit/OpenDreamKit/issues/86#issuecomment-287070822

pip usually requires setuptools and wheel, but the later two are not installed automatically

jupyter nbextension install --py --symlink --sys-prefix ipympl<br>
set symbol link /usr/share/jupyter/nbextensions/jupyter-matplotlib to /usr/lib/python3/dist-packages/ipympl/static<br>
jupyter nbextension enable --py --sys-prefix ipympl<br>
add "jupyter-matplotlib/extension": true to /etc/jupyter/nbconfig/notebook.json

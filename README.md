<h1> To run the Betty linter just with command betty <filename>: </h1>

<h5> Go to the Betty repository </h5> 

<p>
<br> Clone the repo to your local machine
<br> cd into the Betty directory
<br> Install the linter with sudo ./install.sh
</p>

<h5> emacs or vi a new file called betty, and copy the script below: </h5>

<p>
<br> #!/bin/bash
<br> # Simply a wrapper script to keep you from having to use betty-style
<br> # and betty-doc separately on every item.
<br> # Originally by Tim Britton (@wintermanc3r), multiargument added by
<br> # Larry Madeo (@hillmonkey)
<br> BIN_PATH="/usr/local/bin"
<br> BETTY_STYLE="betty-style"
<br> BETTY_DOC="betty-doc"
<br> if [ "$#" = "0" ]; then
<br> echo "No arguments passed."
<br> exit 1
<br> fi
<br> for argument in "$@" ; do
<br> echo -e "\n========== $argument =========="
<br> ${BIN_PATH}/${BETTY_STYLE} "$argument"
<br> ${BIN_PATH}/${BETTY_DOC} "$argument"
<br> done
</p>

<h3> Once saved, exit file and change permissions to apply to all users with chmod a+x betty </h3>
<h3> Move the betty file into /bin/ directory or somewhere else in your $PATH with sudo mv betty /bin/ </h3>
<h2> You can now type betty <filename> to run the Betty linter! </h2>

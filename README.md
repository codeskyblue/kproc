# kproc

This is a golang lib, offer a better way to kill all child process.

This lib has been used in [fswatch](https://github.com/codeskyblue/fswatch).

## Usage

	go get -v github.com/codeskyblue/kproc

usage1:

	cmd := exec.Command("sleep", "300")
	p := kproc.SpawnProcCommand(cmd)
	p.Terminate(syscall.SIGINT)

usage2:

	p := kproc.SpawnProcString("sleep 300")
	p.Terminate(syscall.SIGTERM)
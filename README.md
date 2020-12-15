gogo
> ⚠ **The project has stopped maintenance**  
> 👉 It is recommended to use a new solution in your project: [P3TERX/ssh2actions](https://github.com/P3TERX/ssh2actions)  
> 👉 If you just want to connect to the Actions VM via SSH, move to [P3TERX/ActionsVM](https://github.com/P3TERX/ActionsVM)

# Action Debugger

Interactive debugger for GitHub Actions

## Usage

```
steps:
- name: Setup Debug Session
  uses: P3TERX/debugger-action@main
```

In the log for the action you will see:

```
To connect to this session copy-n-paste the following into a terminal or browser:

ssh Y26QeagDtsPXp2mT6me5cnMRd@nyc1.tmate.io

https://tmate.io/t/Y26QeagDtsPXp2mT6me5cnMRd
```
> TIPS: This message is displayed 3 times, every 30 seconds.

Simply follow the instructions and copy the ssh command into your terminal to create an ssh connection the running instance. The session will close immedeatly after closing the ssh connection to the running instance.

There is a global timeout after 30 minutes. This will close any open ssh sessions. To prevent the session from being terminated run:

```
touch /tmp/keepalive
```

## Acknowledgments

* [tmate.io](https://tmate.io)
* Max Schmitt's [action-tmate](https://github.com/mxschmitt/action-tmate)
* Christopher Sexton's [debugger-action](https://github.com/csexton/debugger-action)

### License

The action and associated scripts and documentation in this project are released under the MIT License.

# suckless

1. st 在渲染 colored emoji 时会崩溃, 好像是 xft 字体引擎的问题, 暂时的解决办法是禁用 colored emoji

```bash
sudo apt remove fonts-noto-color-emoji
```

2. dwm 中 vmtools 不生效的问题参考: https://github.com/vmware/open-vm-tools/issues/447#issuecomment-707607317

> You need to start `vmware-user-suid-wrapper` manually. Other window managers
> probably can start `/etc/xdg/autostart/vmware-user.desktop` automatically, but dwm
> does not.
>
> I also need to restart `vmtoolsd` service so that other stuff like resizing window
> works too.

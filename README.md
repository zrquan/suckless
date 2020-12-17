# suckless

1. st 在渲染 colored emoji 时会崩溃, 好像是 xft 字体引擎的问题, 暂时的解决办法是禁用 colored emoji

```bash
sudo apt remove fonts-noto-color-emoji

# and you can use symbola instead
sudo apt install fonts-symbola
```

2. vmtools

install: `sudo apt install open-vm-tools open-vm-tools-desktop`

if vmtools doesn't work, try: https://github.com/vmware/open-vm-tools/issues/447#issuecomment-707607317

> You need to start `vmware-user-suid-wrapper` manually. Other window managers
> probably can start `/etc/xdg/autostart/vmware-user.desktop` automatically, but dwm
> does not.
>
> I also need to restart `vmtoolsd` service so that other stuff like resizing window
> works too.

3. wmname

Java 识别不了 dwm 窗口管理器, 这会导致 Java 的图形程序有各种问题--比如菜单自动消失、窗口尺寸无法改变等等

使用 suckless 提供的工具 [wmname](https://tools.suckless.org/x/wmname/) 可以冒充其他窗口管理器的名称, 解决以上问题

``` bash
wname LG3D
```

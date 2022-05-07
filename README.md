# bilibili2local

bilibili视频命令行下载工具，根据油猴插件修改：https://greasyfork.org/zh-CN/scripts/390952

## 使用

```shell
npm install -g bilibili2local
b2l -u https://www.bilibili.com/video/BV1oA411H7Rc?p=19
```

## 参数

|参数|必选|默认值| 示例 | 含义 |
| -- | -- | -- | -- | -- |
| -u, -uri | 否 | null | https://www.bilibili.com/video/BV1oA411H7Rc?p=19 | ilibili视频网址 |
| -r, -range | 否 | null | 1,30 | 下载集数范围 |
| -o, -output | 否 | dist | video | 输出文件夹 |

**-u -r 参数不传，将会在程序运行中请求输入，主要兼容命令行中特殊字符**

![bilibili download](./b2l.gif)

## 其他

1. 在window的git Bash中不支持显示下载进度条，问题是`progress`不兼容
2. node version > 12
3. 视频为flv格式，一般系统自带播放器无法播放，考虑到视频转换的库都比较大，所以未集成自动转mp4功能，推荐下载个恒星播放器。
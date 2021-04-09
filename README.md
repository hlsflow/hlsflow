# Hlsflow
## Convert videos into hls stream with github action and host it for free


### Why?

- Explore the power of github workflow
- Automate your video conversion work
- Connect cdn with your github repo and publish videos directly from github (For private repo, For public repo use raw.githubusercontent.com)
- No bandwidth limitations
- Host videos for you vlog

### Process

Here i used FFMPEG to convert those videos into hls stream. You can check `convert.sh` for better understanding the process. After conversion has been completed it will push that directory into github.

### How to use?

- Click on `Use This Template` & Generate a repo from this template
- Create a [personal access token](https://github.com/settings/tokens) with `repo` scope
- Come back to your generated repo and go to `Settings` > `Secrets` > `New repository secret`
- Secret name is `GH_TOKEN` (Imp) & Put your Access Token in `Value` Field
- Edit `convert.sh` and put input and output details
- Click Actions click on `Create a Hls Stream` > `Run Workflow` 
- Please don't change anything untill wokflow has been completed


![Process](https://raw.githubusercontent.com/hlsflow/hlsflow/main/process.gif "Process")

- After completed you can stream it like this

    ```
    https://raw.githubusercontent.com/{YOUR_USERNAME}/{YOUR_REPOSITORY_NAME}/main/{OUTPUT_PATH_NAME}/master.m3u8

    Or, Go to output path and find 'master.m3u8' click on that, then click 'raw'
    ```

### Huaah, this is github abuse !

No, This repository has been created for educational purposes. So, I'm not responsible for any kind of abuse. Also pushing some copyright material in your public repo is illegal.

### Credits

- [Setup FFmpeg (Action)](https://github.com/marketplace/actions/setup-ffmpeg)
- [mikeal/publish-to-github-action](https://github.com/mikeal/publish-to-github-action)
- [Vod-Converter](https://gist.github.com/cachecleanerjeet/35d703ee8d1d76f40aa8015d9df5be6f)

### License & Copyright
- This Project is [GPL-3.0 License](https://github.com/hlsflow/hlsflow/blob/main/LICENSE) Licensed
- Copyright 2021 by [Tuhin Kanti Pal](https://github.com/cachecleanerjeet)

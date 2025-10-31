# ha-cloudnas-clouddrive2-addon

Home Assistant加载项，用于集成CloudNAS CloudDrive 2，实现云存储管理功能。


## 安装步骤

### 步骤1：添加加载项仓库到Home Assistant
1. 进入Home Assistant界面，点击**设置**→**加载项**→**加载项商店**。
2. 点击右上角“三点菜单”，选择**存储库**。
3. 输入仓库地址：`https://github.com/Daring47/ha-cloudnas-clouddrive2-addon`，点击**添加**。


### 步骤2：安装并启动加载项
1. 在“加载项商店”中找到“CloudNAS CloudDrive 2”，点击**安装**。
2. 安装完成后，可根据需求调整配置（如端口、时区），然后点击**启动**。


## 配置说明

### 加载项配置
- **端口**：默认映射`8080`端口，若与其他服务冲突可修改`addon.json`的`ports`字段。
- **持久化数据**：配置文件存储在HA的`config/addons_data/ha-cloudnas-clouddrive2/`目录下。
- **环境变量**：可在`addon.json`中调整`TZ`（时区）等变量。


### Web界面访问
加载项启动后，可通过以下地址访问CloudDrive 2的Web界面：
`http://<你的Home Assistant IP>:8080`


## 故障排查
- **日志查看**：在加载项页面点击“日志”，可排查启动或运行时的错误。
- **镜像拉取失败**：若使用私有GitHub镜像，需先让HA的Docker守护进程通过`docker login ghcr.io`认证（使用GitHub个人访问令牌）。


## 版本更新
关注本仓库的Commit记录，在Home Assistant的“加载项商店”中点击“刷新”即可获取更新提示。

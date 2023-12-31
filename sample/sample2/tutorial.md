## First step

Hello world

```bash
ls -a
```

* GCPプロジェクトを選択してください。(選択中のGoogleアカウントがアクセス可能なGCPProjectの一覧が表示されます)

<walkthrough-project-setup></walkthrough-project-setup>

* 選択したProjectIDをset projectするためにexportします。

```bash
export PROJECT_ID=<walkthrough-project-id/>
```

* 選択したProjectIDに対してgcloudコマンドを発行するために設定します。

```bash
gcloud config set project $PROJECT_ID
```

[see](https://cloud.google.com/shell/docs/cloud-shell-tutorials/directives-project-setup?hl=ja)

* 選択したGCPProjectに存在するGCSbucketの一覧を表示します。

```bash
gcloud storage ls 
```

* 選択したGCPProjectに存在するCloudRunの一覧を表示します。(APIを有効にして実行)

APIを有効にする権限がない場合は当然実行できません。
Service Usage ユーザ(serviceusage.services.use)か、Service Usage 管理者serviceusage.services.enable)の権限が必要です

<walkthrough-enable-apis apis="run.googleapis.com"></walkthrough-enable-apis>

```bash
gcloud run services list
```

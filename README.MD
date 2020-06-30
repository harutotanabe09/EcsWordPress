### ECSのインストール

brew install amazon-ecs-cli

### ECSの設定

ecs-cli configure --region ap-northeast-1 --cluster ecs-cli-test

### AWSの設定

aws configure --profile XXXX

### ECSのインストール

ecs-cli up --keypair KEY_NAME --capability-iam --size 2 --instance-type t2.micro  --aws-profile XXXX

### ECSのコンテナ確認

ECSの起動確認

ecs-cli compose -f docker-compose.yml up --aws-profile XXXX

### ECSのコンテナ落とす

ecs-cli compose -f ./docker-compose.yml down --aws-profile XXXX

### ECSのサービスアップ

ecs-cli compose -f ./docker-compose.yml service up

### ECSのコンテナ削除

ecs-cli compose -f ./docker-compose.yml service rm --aws-profile XXXX
ecs-cli down --force --aws-profile XXXX

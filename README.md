//Устанавливаем wget:

sudo yum install wget

//Скачиваем файл репозитория:

sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo

//Устанавливаем docker:

sudo yum install docker-ce docker-ce-cli containerd.io

//Запускаем его и разрешаем автозапуск:

sudo systemctl enable docker --now

//Для этого сначала убедимся в наличие пакета curl.

б) На системы RPM:

sudo yum install curl

COMVER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d\" -f4)

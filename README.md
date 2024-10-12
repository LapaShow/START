//Устанавливаем wget:

yum install wget

//Скачиваем файл репозитория:

wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo

//Устанавливаем docker:

yum install docker-ce docker-ce-cli containerd.io

//Запускаем его и разрешаем автозапуск:

systemctl enable docker --now

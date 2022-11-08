## PG-OSC

tools ini dipake buat alter table, indexing, pokoknya kegiatan db yang lama menjadi lebih indah, menjadi lebih seemles dan insyaallah zero downtime.
ini running di docker pastikan dockernya juga udah di install.

untuk install seperti berikut

```
$ chmod 777 install-pgosc.sh
$ ./install-pgosc.sh
```
untuk runningnya kita pake supervisor untuk daemonnya biar bisa ditinggal. dan berikut filenya.

## Tables

| Name File  | Path File |
| ------------- |:-------------:|
| migrate.conf     | /etc/supervisor/conf.d/migrate.conf     |
| supervisord.conf      | /etc/supervisor/   |
| example-migrate.sh      | /home/$user/   |

file yang harus di sesuaikan

```
$ pgosc-migrate.conf
$ example-pgosc-command.sh
```

setelah semua mantep jalankan

```
$ supervisorctl reload
$ supervisorctl restart
```

## REDIS-RIOT

tools ini dipake buat bantuin kita biar gak usah redis dump kalo mau migrasi atau mau pindah pake migration tool aja biar sat set sat set anjay slebew.
ini running di docker pastikan dockernya juga udah di install.
untuk installer itu udah sekalian pake yang atas udah tinggal pake.

kita juga pake supervisor biar ada daemonnya dan bisa ditinggal tidur aja tenang hirup.

file yang harus di sesuaikan

```
$ redisriot-migrate.conf
$ example-redisriot-command.sh
```



## source

sumber belajar mantep dari sini[pgosc-reffer] (https://github.com/shayonj/pg-osc).
sumber belajar mantep dari sini[redis-riot] (https://developer.redis.com/riot/riot-redis/cookbook.html).
sumber answer issue mantep dari sini [image-running-another-platform] (https://enlear.academy/run-amd64-docker-images-on-an-arm-computer-208929004510)

# simple-dba-tools

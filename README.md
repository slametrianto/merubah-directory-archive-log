# merubah-directory-archive-log-oracle



buat direktory 

mkdir -p /backup/archivelog

chown -R oracle:oinstall /backup/

sql > shutdown immediate
sql > startup mount

sql > alter system set LOG_ARCHIVE_DEST_1='LOCATION=/backup/archivelog/';

sql > startup

sql > archive log list;

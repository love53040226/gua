worker_processes  1;

events {
    worker_connections  1024;
}

rtmp {
    server {
        listen 1935;
        chunk_size 4096;

        application live1 {
            live on;
            record off;
        }
    }
}

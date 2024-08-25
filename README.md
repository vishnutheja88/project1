# project1
sample_project_1


$ dotnet run --project HelloWorldApp.csproj


vi /etc/nginx/sites-available/default

server {
    listen        80;
    server_name   _;          #azurewebsites.net *.azurewebsites.net;
    location / {
        proxy_pass         http://localhost:5144;
        proxy_http_version 1.1;
        proxy_set_header   Upgrade $http_upgrade;
        proxy_set_header   Connection keep-alive;
        proxy_set_header   Host $host;
        proxy_cache_bypass $http_upgrade;
        proxy_set_header   X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header   X-Forwarded-Proto $scheme;
    }
}

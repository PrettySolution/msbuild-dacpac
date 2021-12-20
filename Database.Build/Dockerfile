FROM mcr.microsoft.com/dotnet/core/sdk:3.1.416 AS build
WORKDIR /src
COPY ["CrtxAdmin/CrtxAdmin.csproj", "CrtxAdmin/"]
COPY ["Database.Build/Database.Build.csproj", "Database.Build/"]
RUN dotnet restore "Database.Build/Database.Build.csproj"
COPY . .
WORKDIR "/src/Database.Build"
RUN dotnet build "Database.Build.csproj" -c Release -o /app/build
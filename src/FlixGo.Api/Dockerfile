FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["src/FlixGo.Api/FlixGo.Api.csproj", "src/FlixGo.Api/"]
RUN dotnet restore "src/FlixGo.Api/FlixGo.Api.csproj"
COPY . .
WORKDIR "/src/src/FlixGo.Api"
RUN dotnet build "FlixGo.Api.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "FlixGo.Api.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "FlixGo.Api.dll"]

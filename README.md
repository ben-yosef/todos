# שלב 1: בניית הפרויקט
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /app

# העתקת קבצי הפרויקט והתקנת תלויות
COPY . ./
RUN dotnet restore
RUN dotnet publish -c Release -o out

# שלב 2: הרצת השרת
FROM mcr.microsoft.com/dotnet/aspnet:8.0
WORKDIR /app
COPY --from=build /app/out .

# פתיחת הפורט שבו השרת מאזין (במקרה שלך 5073)
EXPOSE 5073

# הפעלת השרת
ENTRYPOINT ["dotnet", "YourProjectName.dll"]
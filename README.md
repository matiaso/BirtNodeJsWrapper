BirtNodeJsWrapper is nodejs server for reporting from birt.
Aby zainstalować należy:
0. Pobrać i zainstalować nodejs.
1. Pobrać repo z gita.
2. Pobrać Latest BIRT Runtime Release Build. Rozpakować.
3. Dodać zmienną środowiskową BIRT_HOME np. export BIRT_HOME=$HOME/birt-runtime-4_5_0.
4. Skopiować folder ReportEngine do poprzednio pobranego repo z gita.
5. Dodać folder Reports/Temp gdzie należy umieścić pliki *.rptdesign.
6. npm install node-uuid w repo.
7. Na windowsie w pliku genReport.bat zmienić:
set BIRTCLASSPATH=
for %%i in (%BIRT_HOME%\ReportEngine\lib\*.jar) do set BIRTCLASSPATH=%%i;!BIRTCLASSPATH!
na:
SET BIRTCLASSPATH=%BIRT_HOME%\ReportEngine\lib\*

v_0.1.1
# configuraciones_escaneres
config en la nube para actualizar dinamicamente config escaneres alta velocidad en remoto.

Config dividido en dos: 
- config con paths y cadenas conexion bbdd
  - cordoba
  - malaga 
- config con resto paramtros: camara, coms, recorte imagen, cabecera

Existe un 3er fichero config --> listadoMaquinas.yml donde se encuentran las coincidencias SN <-> numero de maquina de escaneo

# instalacion git Windows
1. py -m pip install gitpython
2. descargar e instalar git para windows --> https://github.com/git-for-windows/git/releases/download/v2.46.0.windows.1/Git-2.46.0-64-bit.exe
   instalar todo por defecto al instalar git en windows
3. ejecutar en la cmd de windows
   - set GIT_PYTHON_GIT_EXECUTABLE="C:\Program Files\Git\cmd\git.exe"
   - %GIT_PYTHON_GIT_EXECUTABLE% --version
   - set GIT_PYTHON_GIT_EXECUTABLE=C:\Program Files\Git\cmd\git.exe
![image](https://github.com/user-attachments/assets/502a4c6b-c22f-4c84-b65a-33e7fe5feb35)
4. necesario reiniciar el equipo 

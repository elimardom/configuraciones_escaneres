v_0.1.2
# Actualizaciones OTA escanerAV -- configs + sw

### configuraciones_escaneres
config en la nube para actualizar dinamicamente config escaneres alta velocidad en remoto.

Config dividido en dos: 
- config con paths y cadenas conexion bbdd
  - cordoba
  - malaga 
- config con resto paramtros: camara, coms, recorte imagen, cabecera

Existe un 3er fichero config --> listadoMaquinas.yml donde se encuentran las coincidencias SN <-> numero de maquina de escaneo

### actualizaciones ota de la app de escaneo
Cambiando la version en el config de la maquina que queremos actualizar se fuerza la actualizacion automatica del sw de escaneo.
- main_camara_funciones.exe --> ejecutable de la aplicacion compilada
- launcher.exe --> para pivotar entre la version de sw antigua y la nueva recogida de Git

el launcher tambien se actualiza de manera remota 
  
![image](https://github.com/user-attachments/assets/a6edc535-49be-459e-8534-f96bd469da89)




# Para desplegar
### instalacion git Windows
1. py -m pip install gitpython
2. descargar e instalar git para windows --> https://github.com/git-for-windows/git/releases/download/v2.46.0.windows.1/Git-2.46.0-64-bit.exe
   instalar todo por defecto al instalar git en windows
3. ejecutar en la cmd de windows
   - set GIT_PYTHON_GIT_EXECUTABLE="C:\Program Files\Git\cmd\git.exe"
   - %GIT_PYTHON_GIT_EXECUTABLE% --version
   - set GIT_PYTHON_GIT_EXECUTABLE=C:\Program Files\Git\cmd\git.exe
![image](https://github.com/user-attachments/assets/502a4c6b-c22f-4c84-b65a-33e7fe5feb35)
4. necesario reiniciar el equipo

### preparación nueva maquina con sw ota (sw + config)
1. instalar git punto anterior
2. pull repositorio camara-lineal-procesos-alto-nivel para poder comprobar el SN de la maquina
3. ejecutar serial_arduino para identificar al nuevo equipo e incluirlo en listadoMaquinas.yml
4. configurar en el repositorio configuraciones_escaneres --> config nuevo de la maquina que se vaya a registrar --> config[NumeroMaquina].yml ej: config2.yml

**el serial number detectado es el del arduino main mega --> si por mantenimiento este dispositivo se cambia hay que registrar su nuevo SN en el archivo listadoMaquinas.yml




# Contributing
Area Electronica
# License
Copyright (c) 2024, JOSMAR INDA GROUP, S.L.






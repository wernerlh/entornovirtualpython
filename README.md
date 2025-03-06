## Guía para crear y gestionar un entorno virtual en Python
Estos pasos te servirán para crear entornos virtuales. Incluiremos un ejemplo de un proyecto que utiliza la biblioteca flask.
### Primer paso: Crear el entorno virtual

```bash
virtualenv -p python3 env
```

### Segundo paso: Activar el entorno virtual

En Windows:

```bash
.\env\Scripts\activate
```

En caso de error, establece la política de ejecución:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope Process
```

Para verificar:

```powershell
Get-ExecutionPolicy
```

En macOS/Linux:

```bash
source env/bin/activate
```

### Tercer paso: Actualizar pip (opcional)

```bash
python -m pip install --upgrade pip
```

### Cuarto paso: Instalar los paquetes necesarios

```bash
pip install nombre_del_paquete
```

### Quinto paso: Guardar las dependencias en un archivo

```bash
pip freeze > requirements.txt
```

En caso que quieres desactivar el entorno virtual sigues con este paso:

### Sexto paso: Desactivar el entorno virtual

```bash
deactivate
```

Con estos pasos, podrás crear, activar, mantener y desactivar un entorno virtual en Python de manera eficiente.

### Proyecto sin entorno virtual pero con `requirements.txt`

Para activar un proyecto utilizando un archivo `requirements.txt`, repite los pasos 1, 2 y 3 (opcional), y luego continúa con:

### Cuarto paso: Instalar paquetes desde un archivo `requirements.txt`

```bash
pip install -r requirements.txt
```


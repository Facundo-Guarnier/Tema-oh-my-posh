# Tema personalizado de Oh-my-posh

<div align="center">
 <img src="https://github.com/Facundo-Guarnier/Tema-oh-my-posh/blob/main/Ejemplo.png" alt="Ejemplo" style="border-radius: 15px;">
</div>

## Intalar tema

### 1. PowerShell

Ejecutar lo siguiente:

`notepad $PROFILE`

Agregar las siguientes lineas:

        #-- Oh-my-posh
        (@(& 'ruta-de-instalacion-oh-my-posh-.exe' init pwsh --config='ruta-del-tema-.omp.json' --print) -join "`n") | Invoke-Expression
        Import-Module Terminal-Icons
        Set-PSReadLineOption -PredictionViewStyle ListView
        #-- Oh-my-posh

### 2. Bash

Ejecutar lo siguiente:

`nano .bashrc`

Agregar las siguientes lineas:

        #-- Oh-my-posh
        export OMP_CONFIGURE_SUDO=true
        export POWERLEVEL9K_MODE="awesome-fontconfig"
        export POWERLEVEL9K_AWESOME_FONT="ruta-de-la-fuente-.ttf"
        eval "$(oh-my-posh init bash --config ruta-del-tema-.omp.json)"
        #-- Oh-my-posh

## Aclaraciones del archivo .omp.json

* Los bloques son las "areas" donde aparecerán los segmentos. Los bloques se puede alinear a la izquierda o derecha o hacer un salto de linea nuevo.
* Los segmentos son las distintas informaciones a mostar. Ej: Usuario, path, hora, ram usada.

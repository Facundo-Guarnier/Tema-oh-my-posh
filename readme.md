# Intalar tema

## En windwos

Abrir el archivo:

`notepad $PROFILE`

Agregar las siguientes lineas:

> #-- Oh-my-posh
> (@(& 'ruta-de-instalacion-oh-my-posh-.exe' init pwsh --config='ruta-del-tema-.omp.json' --print) -join "`n") | Invoke-Expression
> Import-Module Terminal-Icons
> Set-PSReadLineOption -PredictionViewStyle ListView
> #-- Oh-my-posh

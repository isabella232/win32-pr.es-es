---
description: Si la acción InstallValidate detecta la instalación de un archivo en uso, muestra el cuadro de diálogo FilesInUse y registra la siguiente información.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registro de solicitudes de reinicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae5131d5662b4064538a9ae80936d6a02e74edbe44a725d5dd27754a9a2e845c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043065"
---
# <a name="logging-of-reboot-requests"></a>Registro de solicitudes de reinicio

Si la [acción InstallValidate](installvalidate-action.md) detecta la instalación de un archivo en uso, muestra el cuadro de [diálogo FilesInUse](filesinuse-dialog.md) y registra la siguiente información.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

Si el instalador detecta que está a punto de sobrescribir un archivo que está en uso, registra la siguiente información.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

El \[ token de nombre de archivo puede contener realmente una ruta de acceso a un archivo con una extensión \] .rbf. En este caso, el archivo .rbf es realmente el archivo original registrado por el mensaje 1603 cuyo nombre se ha cambiado al archivo .rbf. Primero se cambia el nombre del archivo que está en uso con una extensión .rbf y, a continuación, se elimina.

Para obtener más información sobre por qué el instalador está intentando sobrescribir este archivo determinado, puede usar la opción de registro detallado. Use el valor INSTALLLOGMODE VERBOSE en una llamada \_ a [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o use la opción de salida detallada de Las opciones [de la línea de comandos](command-line-options.md). Esto registra la siguiente información.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

El registro incluirá un mensaje como "El archivo existente es una versión inferior" o "El archivo existente está dañado (suma de comprobación no válida)"

 

 




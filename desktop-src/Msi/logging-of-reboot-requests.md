---
description: Si la acción InstallValidate detecta la instalación de un archivo en uso, muestra el cuadro de diálogo FilesInUse y registra la información siguiente.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registro de solicitudes de reinicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547003"
---
# <a name="logging-of-reboot-requests"></a>Registro de solicitudes de reinicio

Si la [acción InstallValidate](installvalidate-action.md) detecta la instalación de un archivo en uso, muestra el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) y registra la información siguiente.

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

El \[ token de nombre de archivo \] puede contener realmente una ruta de acceso a un archivo con una extensión. Rbf. En este caso, el archivo. Rbf es realmente el archivo original registrado por el mensaje 1603, al que se le ha cambiado el nombre al archivo. Rbf. Primero se cambia el nombre del archivo que se está usando con una extensión. Rbf y, a continuación, se elimina.

Para obtener más información acerca de por qué el instalador está intentando sobrescribir este archivo en particular, puede usar la opción de registro detallado. Use el \_ valor detallado de INSTALLLOGMODE en una llamada a [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o use la opción de salida detallada de las [Opciones](command-line-options.md)de la línea de comandos. Esto registra la siguiente información.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

El registro incluirá un mensaje como "el archivo existente es una versión anterior" o "el archivo existente está dañado (suma de comprobación no válida)"

 

 




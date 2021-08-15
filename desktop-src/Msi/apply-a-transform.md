---
description: El archivo VBScript WiUseXfm.vbs se proporciona en los componentes Windows SDK para Windows instaladores. En este ejemplo se muestra cómo se puede usar el script para aplicar una transformación a una base de datos Windows installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001737b1a08ea33ce233fa0aad90e96e23a1079f2c28f9d6308219cba270f6ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381614"
---
# <a name="apply-a-transform"></a>Aplicar una transformación

El archivo VBScript WiUseXfm.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se puede usar el script para aplicar una transformación a una base de datos Windows installer.

En el ejemplo se muestra el uso de

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)

Necesitará la versión CScript.exe o WScript.exe de Windows host de script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiUseXfm.vbs ruta de \[ acceso a la base de datos original para transformar las opciones de \] \[ \] \[ archivo\]**

Especifique la ruta de acceso a la base Windows de datos del instalador. Especifique la ruta de acceso al archivo de transformación. Si se omite la ruta de acceso al archivo de transformación, solo se comparan las dos bases de datos. El tercer argumento es un valor numérico opcional que especifica un conjunto de condiciones de error que se van a suprimir. Agregue estos valores juntos para suprimir varias condiciones.



| Valor | Condición de error que se suprimirá                   |
|-------|-----------------------------------------------|
| 1     | Agregar una fila que ya existe.             |
| 2     | Eliminar una fila que no existe.           |
| 4     | Agregar una tabla que ya existe.           |
| 8     | Eliminar una tabla que no existe.         |
| 16    | Actualizar una fila que no existe.           |
| 256   | Error de coincidencia de páginas de códigos de base de datos y transformación. |



 

Para obtener ejemplos de scripting adicionales, [Windows Ejemplos de scripting del instalador .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de](windows-installer-development-tools.md)desarrollo del instalador .

 

 




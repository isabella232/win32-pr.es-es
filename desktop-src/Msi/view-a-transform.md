---
description: El archivo VBScript WiLstXfm.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. Este ejemplo de script se puede usar para ver un archivo de transformación.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Ver una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f599099ff858275f3b0c75df9b265129adfe0659a5c3c35d285417a8e295f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995635"
---
# <a name="view-a-transform"></a>Ver una transformación

El archivo VBScript WiLstXfm.vbs se proporciona en el [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo de script se puede usar para ver un archivo de transformación.

En el ejemplo se muestra el uso de:

-   [\_Tabla TransformView](-transformview-table.md)
-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)
-   [**Propiedad IsNull**](record-isnull.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto Record**](record-object.md)

El uso de este ejemplo requiere la CScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiLstXfm.vbs** ruta de acceso a la ruta de acceso de la opción de base de datos *\[ de referencia que se \] \[ va a transformar para que \] \[ se vea. \]*

Especifique la ruta de acceso a la base de datos del instalador Windows referencia. Especifique una lista de rutas de acceso para transformar los archivos que se están visualizando. Cada ruta de acceso de la lista puede ir precedida de un valor numérico opcional. Este valor especifica un conjunto de condiciones de error que se van a suprimir. Puede agregar estos valores juntos para suprimir varias condiciones. Si no se especifica ninguna opción numérica, se suprimen todas las condiciones de error. Los argumentos de esta lista se ejecutan en el orden de izquierda a derecha en el que aparecen en la línea de comandos.



| Value | Condición de error que se suprimirá                   |
|-------|-----------------------------------------------|
| 1     | Agregar una fila que ya existe.             |
| 2     | Eliminar una fila que no existe.           |
| 4     | Agregar una tabla que ya existe.           |
| 8     | Eliminar una tabla que no existe.         |
| 16    | Actualizar una fila que no existe.           |
| 256   | Error de coincidencia de páginas de códigos de base de datos y transformación. |



 

Para obtener ejemplos de scripting adicionales, [Windows Ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de](windows-installer-development-tools.md)desarrollo del instalador .

 

 




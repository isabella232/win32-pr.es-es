---
description: El WiLstXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo de script se puede usar para ver un archivo de transformación.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Ver una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652409"
---
# <a name="view-a-transform"></a>Ver una transformación

El WiLstXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo de script se puede usar para ver un archivo de transformación.

En el ejemplo se muestra el uso de:

-   [\_Tabla TransformView](-transformview-table.md)
-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)
-   [**Propiedad IsNull**](record-isnull.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)

El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiLstXfm.vbs** *\[ ruta de acceso de referencia de la opción de base \] \[ de datos a la \] \[ transformación que se va a ver \]*

Especifique la ruta de acceso a la base de datos de Windows Installer de referencia. Especifique una lista de rutas de acceso para transformar los archivos que se están viendo. Cada ruta de acceso de la lista puede ir precedida de un valor numérico opcional. Este valor especifica un conjunto de condiciones de error que se van a suprimir. Puede agregar estos valores juntos para suprimir varias condiciones. Si no se especifica ninguna opción numérica, se suprimen todas las condiciones de error. Los argumentos de esta lista se ejecutan en el orden de izquierda a derecha en el que aparecen en la línea de comandos.



| Value | Condición de error que se va a suprimir                   |
|-------|-----------------------------------------------|
| 1     | Agregando una fila que ya existe.             |
| 2     | Eliminar una fila que no existe.           |
| 4     | Agregando una tabla que ya existe.           |
| 8     | Eliminando una tabla que no existe.         |
| 16    | Actualizar una fila que no existe.           |
| 256   | No coinciden las páginas de códigos de base de datos y de transformación. |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




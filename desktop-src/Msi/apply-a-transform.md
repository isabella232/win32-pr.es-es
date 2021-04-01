---
description: El WiUseXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se puede utilizar el script para aplicar una transformación a una base de datos de Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909105"
---
# <a name="apply-a-transform"></a>Aplicar una transformación

El WiUseXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se puede utilizar el script para aplicar una transformación a una base de datos de Windows Installer.

En el ejemplo se muestra el uso de

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiUseXfm.vbs \[ ruta de acceso a la ruta de acceso de base de datos original \] \[ para transformar opciones de archivo \] \[\]**

Especifique la ruta de acceso a la base de datos Windows Installer. Especifique la ruta de acceso al archivo de transformación. Si se omite la ruta de acceso al archivo de transformación, las dos bases de datos solo se comparan. El tercer argumento es un valor numérico opcional que especifica un conjunto de condiciones de error que se van a suprimir. Agregue estos valores juntos para suprimir varias condiciones.



| Value | Condición de error que se va a suprimir                   |
|-------|-----------------------------------------------|
| 1     | Agregando una fila que ya existe.             |
| 2     | Eliminar una fila que no existe.           |
| 4     | Agregando una tabla que ya existe.           |
| 8     | Eliminando una tabla que no existe.         |
| 16    | Actualizar una fila que no existe.           |
| 256   | No coinciden las páginas de códigos de base de datos y de transformación. |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




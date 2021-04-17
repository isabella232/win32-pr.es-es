---
description: El WiExport.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687190"
---
# <a name="export-files"></a>Exportar archivos

El WiExport.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo escribir un script para exportar tablas a una base de datos de Windows Installer. El ejemplo de script se conecta a un objeto de [**instalador**](installer-object.md) , abre una base de datos y exporta las tablas a los archivos de almacenamiento.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método Export**](database-export.md)
-   [**Método OpenView**](database-openview.md) del [ **objeto Database**](database-object.md)
-   [**Método fetch**](view-fetch.md) del [ **objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiExport.vbs \[ ruta de acceso de la base de datos \] \[ a la \] \[ lista de nombres de \] \[ tabla de opciones de carpeta\]**

Especifique la ruta de acceso a la base de datos del instalador desde la que se exportan las tablas. Especifique la ruta de acceso a la carpeta en la que se copiarán los archivos de almacenamiento exportados. Enumera los nombres que distinguen mayúsculas de minúsculas de las [tablas de base de datos](database-tables.md) que se van a exportar. Especifique ' \* ' para exportar todas las tablas, incluido \_ SummaryInformation.

Las siguientes opciones se pueden especificar en cualquier parte de la línea de comandos antes de la lista de nombres de tabla.



| Opción              | Descripción                                            |
|---------------------|--------------------------------------------------------|
| no se ha especificado ninguna opción | Los archivos de almacenamiento exportados pueden tener un nombre de archivo largo.      |
| /s                  | Fuerce que los archivos de almacenamiento exportados tengan nombres de archivo cortos. |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




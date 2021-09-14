---
description: El archivo VBScript WiExport.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158423"
---
# <a name="export-files"></a>Exportar archivos

El archivo vbscript WiExport.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo escribir script para exportar tablas a una base de datos Windows Installer. El ejemplo de script se conecta a un [**objeto Installer,**](installer-object.md) abre una base de datos y exporta tablas a archivos de archivo.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método de exportación**](database-export.md)
-   [**Método OpenView**](database-openview.md) del objeto [ **Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md) del [ **objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto Record**](record-object.md)

Necesitará la versión de CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiExport.vbs cscript a la ruta de acceso de la \[ base de datos a la lista de nombres de tabla de opciones de \] \[ \] \[ \] \[ carpeta\]**

Especifique la ruta de acceso a la base de datos del instalador desde la que se exportan las tablas. Especifique la ruta de acceso a la carpeta en la que se van a copiar los archivos de archivo exportados. Enumera los nombres que distinguen mayúsculas de minúsculas de las tablas [de base de datos que](database-tables.md) se exportan. Especifique ' \* ' para exportar todas las tablas, incluida \_ SummaryInformation.

Las siguientes opciones se pueden especificar en cualquier lugar de la línea de comandos antes de la lista de nombres de tabla.



| Opción              | Descripción                                            |
|---------------------|--------------------------------------------------------|
| no se ha especificado ninguna opción | Los archivos de archivo exportados pueden tener un nombre de archivo largo.      |
| /s                  | Forzar que los archivos de archivo exportados tengan nombres de archivo cortos. |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




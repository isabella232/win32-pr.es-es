---
description: El WiImport.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos de Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652508"
---
# <a name="import-files"></a>Importar archivos

El WiImport.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos de Windows Installer.

El script se conecta a un objeto del [**instalador**](installer-object.md) , abre una base de datos, procesa una lista de archivos y confirma los cambios antes de cerrar la base de datos.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método Import**](database-import.md)
-   [**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, use la siguiente sintaxis en el símbolo del sistema.

**cscript WiImport.vbs \[ ruta de acceso de la base de datos \] \[ a opciones de carpeta \] \[ lista de archivos de \] \[ almacenamiento**\]

La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

Especifique la ruta de acceso a una base de datos de Windows Installer que se va a crear o que va a recibir las tablas importadas. Especifique la ruta de acceso a la carpeta que contiene los archivos de almacenamiento de las tablas que se van a importar. Enumera los nombres de los archivos de almacenamiento que se van a importar. Los nombres de archivo comodín, como \* . IDT, se pueden usar para importar varios archivos.

Las siguientes opciones se pueden especificar en cualquier parte de la línea de comandos antes de la lista de archivos.



| Opción              | Descripción                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Importe la lista de archivos de almacenamiento de tabla de la carpeta especificada en la base de datos de Windows Installer.                                |
| /C                  | Cree una base de datos de Windows Installer y, a continuación, importe la lista de archivos de almacenamiento de tabla de la carpeta especificada en la nueva base de datos. |



 

Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) para obtener ejemplos adicionales de scripting. Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

Tenga en cuenta que [un ejemplo de localización](a-localization-example.md) también muestra la [importación de tablas de error y de ActionText localizadas](importing-localized-error-and-actiontext-tables.md).

 

 




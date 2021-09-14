---
description: El archivo VBScript WiImport.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones. En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074446"
---
# <a name="import-files"></a>Importar archivos

El archivo vbscript WiImport.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo escribir un script para importar tablas en una base de datos Windows Installer.

El script se conecta a un objeto [**Installer,**](installer-object.md) abre una base de datos, procesa una lista de archivos y confirma los cambios antes de cerrar la base de datos.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método Import**](database-import.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)

Necesitará la versión de CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, use la sintaxis siguiente en el símbolo del sistema.

**cscript WiImport.vbs ruta de acceso a la ruta de acceso de \[ la base de datos a la lista de archivos de archivo de opciones \] \[ de \] \[ \] \[ carpeta**\]

Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

Especifique la ruta de acceso a Windows base de datos del instalador que se va a crear o que va a recibir las tablas importadas. Especifique la ruta de acceso a la carpeta que contiene los archivos de archivo de las tablas que se van a importar. Enumera los nombres de los archivos de archivo que se van a importar. Los nombres de archivo comodín, \* como .idt, se pueden usar para importar varios archivos.

Las siguientes opciones se pueden especificar en cualquier lugar de la línea de comandos antes de la lista de archivos.



| Opción              | Descripción                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Importe la lista de archivos de archivo de tabla de la carpeta especificada en la base de datos Windows installer.                                |
| /C                  | Cree una base Windows installer y, a continuación, importe la lista de archivos de archivo de tabla de la carpeta especificada en la nueva base de datos. |



 

Para obtener más información, vea [Windows de scripting del instalador para](windows-installer-scripting-examples.md) obtener ejemplos de scripting adicionales. Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

Tenga en cuenta [que un ejemplo de localización](a-localization-example.md) también muestra la importación de tablas Error localizado y [ActionText](importing-localized-error-and-actiontext-tables.md).

 

 




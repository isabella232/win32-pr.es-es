---
description: El archivo VBScript WiImport.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. En este ejemplo se muestra cómo escribir un script para importar tablas en una base de Windows installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc67cc3f698d1268a5ce08fe1e4c76b86a425216396fa168b0e8e6dc8a3f91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043865"
---
# <a name="import-files"></a>Importar archivos

El archivo VBScript WiImport.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo escribir un script para importar tablas en una base de Windows installer.

El script se conecta a un objeto [**Installer,**](installer-object.md) abre una base de datos, procesa una lista de archivos y confirma los cambios antes de cerrar la base de datos.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método Import**](database-import.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)

Necesitará la versión CScript.exe o WScript.exe host de script Windows usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, use la sintaxis siguiente en el símbolo del sistema.

**cscript WiImport.vbs ruta de \[ acceso a la ruta de acceso de la base de datos a la lista de archivos \] \[ de archivo de opciones \] \[ \] \[ de carpeta**\]

Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

Especifique la ruta de acceso a Windows base de datos del instalador que se va a crear o que va a recibir las tablas importadas. Especifique la ruta de acceso a la carpeta que contiene los archivos de archivo de las tablas que se van a importar. Enumera los nombres de los archivos de archivo que se van a importar. Los nombres de archivo comodín, \* como .idt, se pueden usar para importar varios archivos.

Las siguientes opciones se pueden especificar en cualquier lugar de la línea de comandos antes de la lista de archivos.



| Opción              | Descripción                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Importe la lista de archivos de archivo de tabla de la carpeta especificada en la base de datos Windows instalador.                                |
| /C                  | Cree una base Windows installer y, a continuación, importe la lista de archivos de archivo de tabla de la carpeta especificada en la nueva base de datos. |



 

Para obtener más información, vea [Windows de scripting del instalador para](windows-installer-scripting-examples.md) obtener ejemplos de scripting adicionales. Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

Tenga en cuenta [que un ejemplo de localización](a-localization-example.md) también muestra la importación de tablas De error localizada y [ActionText](importing-localized-error-and-actiontext-tables.md).

 

 




---
description: El WiStream.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Administrar secuencias binarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678252"
---
# <a name="manage-binary-streams"></a>Administrar secuencias binarias

El WiStream.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se puede utilizar el script para administrar secuencias binarias en una base de datos de Windows Installer. El ejemplo se puede usar para especificar archivadores de archivos comprimidos en una base de datos. Este ejemplo muestra el funcionamiento de la [ \_ tabla streams](-streams-table.md) en la base de datos Windows Installer.

En el ejemplo también se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)
-   [**Fetch (método)**](view-fetch.md)
-   [**Modify (método)**](view-modify.md)
-   [**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md)
-   [**Método SetStream**](record-setstream.md) del [ **objeto record**](record-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiStream.vbs \[ ruta de acceso de la base de datos \] \[ al \] \[ \] \[ nombre del flujo de opciones de archivo\]**

Especifique la ruta de acceso a la base de datos de Windows Installer que va a recibir la secuencia. Especifique una ruta de acceso al archivo binario que contiene los datos de la secuencia. Para enumerar las secuencias en la base de datos del instalador, omita esta ruta de acceso. Puede especificar un nombre de flujo opcional, si se omite, se toma como valor predeterminado el nombre de archivo.

Se puede especificar la opción siguiente.



| Opción              | Descripción                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Agregue una secuencia a la base de datos Windows Installer.                                                 |
| /d                  | Quitar un flujo. Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar. |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




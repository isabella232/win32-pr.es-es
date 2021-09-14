---
description: El archivo VBScript WiStream.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Administrar archivos binarios Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071923"
---
# <a name="manage-binary-streams"></a>Administrar archivos binarios Secuencias

El archivo VBScript WiStream.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se puede usar el script para administrar secuencias binarias en una base de Windows installer. El ejemplo se puede usar para escribir archivadores de archivos comprimidos en una base de datos. En este ejemplo se muestra el funcionamiento de la tabla [ \_ Secuencias en](-streams-table.md) la base de datos Windows Installer.

En el ejemplo también se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método CreateRecord**](installer-createrecord.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md)
-   [**Modify (método)**](view-modify.md)
-   [**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md)
-   [**Método SetStream**](record-setstream.md) del [ **objeto Record**](record-object.md)

Necesitará la versión CScript.exe o WScript.exe host de script Windows para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiStream.vbs cscript a \[ la ruta de acceso de la base de datos al nombre del flujo de \] \[ opciones \] \[ \] \[ de archivo\]**

Especifique la ruta de acceso a la Windows del instalador que va a recibir la secuencia. Especifique una ruta de acceso al archivo binario que contiene los datos de flujo. Para enumerar los flujos de la base de datos del instalador, omita esta ruta de acceso. Puede especificar un nombre de flujo opcional, si se omite, el valor predeterminado es el nombre de archivo.

Se puede especificar la siguiente opción.



| Opción              | Descripción                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Agregue una secuencia a la base de datos Windows installer.                                                 |
| /d                  | Quite una secuencia. Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar. |



 

Para obtener ejemplos de scripting adicionales, [vea Windows de scripting del instalador.](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, vea Windows Herramientas de desarrollo [del instalador .](windows-installer-development-tools.md)

 

 




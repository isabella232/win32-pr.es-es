---
description: El archivo VBScript WiSubStg.vbs se proporciona en los componentes del SDK de Windows para desarrolladores Windows Installer.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Administración de subalmacenamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f6d3a0716854755e595133771ede65b11212cdd0fd19b4502bab0c631a9d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945600"
---
# <a name="manage-substorages"></a>Administración de subalmacenamientos

El archivo vbscript WiSubStg.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo se puede usar el script para administrar subalmacenamientos en una base de datos Windows Installer. Se puede agregar una transformación a una base de datos Windows Installer existente como un subalmacenamiento.

En el ejemplo se muestra el uso de:

-   [\_Tabla de almacenamientos](-storages-table.md)
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

Necesitará la versión de CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**cscript WiSubStg.vbs \[ de acceso a la ruta de acceso de la base de datos al nombre \] \[ de \] \[ \] \[ subalmacenamiento de opciones de archivo\]**

Especifique la ruta de acceso a la base Windows del instalador para agregar o quitar el subalmacenamiento. Especifique una ruta de acceso al archivo de transformación o base de datos que se va a agregar como subalmacenamiento. Para enumerar los subalmacenamientos en la base Windows del instalador, omita la ruta de acceso a este archivo. Puede especificar un nombre de subalmacenamiento opcional, si se omite, el nombre de subalmacenamiento tiene como valor predeterminado el nombre de archivo.

Se puede especificar la siguiente opción.



| Opción              | Descripción                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Agregue un subalmacenamiento a la base de Windows installer.                                                 |
| /d                  | Quite un subalmacenamiento. Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar. |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Installer Development Tools](windows-installer-development-tools.md).

Tenga en [cuenta que un ejemplo de localización](a-localization-example.md) muestra la [inserción de transformaciones de personalización como subalmacenamiento.](embedding-customization-transforms-as-substorage.md)

 

 




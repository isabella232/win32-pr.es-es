---
description: El WiSubStg.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Administrar subalmacenamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361394"
---
# <a name="manage-substorages"></a>Administrar subalmacenamientos

El WiSubStg.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se puede utilizar el script para administrar los subalmacenamientos en una base de datos de Windows Installer. Una transformación puede agregarse a una base de datos de Windows Installer existente como un subalmacenamiento.

En el ejemplo se muestra el uso de:

-   [\_Tabla Storages](-storages-table.md)
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

**cscript WiSubStg.vbs \[ ruta de acceso a la ruta de acceso de la base \] \[ de datos al \] \[ nombre del \] \[ subalmacenamiento de opciones\]**

Especifique la ruta de acceso a la base de datos Windows Installer para agregar o quitar el subalmacenamiento. Especifique una ruta de acceso al archivo de base de datos o de transformación que se va a agregar como subalmacenamiento. Para enumerar los subalmacenamientos en la base de datos Windows Installer, omita la ruta de acceso a este archivo. Puede especificar un nombre de subalmacenamiento opcional, si se omite, el nombre del subalmacenamiento tiene como valor predeterminado el nombre de archivo.

Se puede especificar la opción siguiente.



| Opción              | Descripción                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción | Agregue un subalmacenamiento a la base de datos Windows Installer.                                                 |
| /d                  | Quitar un subalmacenamiento. Esta marca de opción debe ir seguida del nombre del subalmacenamiento que se va a quitar. |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

Tenga en cuenta que [un ejemplo de localización muestra la](a-localization-example.md) [incrustación de transformaciones de personalización como subalmacenamiento](embedding-customization-transforms-as-substorage.md).

 

 




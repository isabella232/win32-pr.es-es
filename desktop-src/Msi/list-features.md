---
description: El WiFeatur.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Enumerar características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360610"
---
# <a name="list-features"></a>Enumerar características

El WiFeatur.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se utiliza el script para mostrar las características de una base de datos de Windows Installer. En este ejemplo se muestra cómo agregar columnas temporales a una base de datos de Windows Installer de solo lectura.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), el [**Método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método Execute**](view-execute.md) y [**método fetch**](view-fetch.md) del [**objeto View**](view-object.md)
-   [**Método OpenView**](database-openview.md), la [**propiedad TablePersistent**](database-tablepersistent.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del [**objeto Database**](database-object.md)
-   [**Propiedad FieldCount**](record-fieldcount.md), [**propiedad IntegerData**](record-integerdata.md)y la [**propiedad StringData**](record-stringdata.md) del [**objeto record**](record-object.md)

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiFeatur.vbs \[ ruta de acceso al nombre de la característica de base de datos \] \[\]**

Especifique la ruta de acceso a la base de datos Windows Installer. Especifique el nombre de la característica. Esto debe aparecer en la columna característica de la [tabla de características](feature-table.md). Si se omite el nombre de la característica, todas las características se muestran como un árbol de características. Si se usa un asterisco ( \* ) como nombre de la característica, WiFeatur.vbs muestra la composición de todas las características. Tenga en cuenta que las bases de datos de gran tamaño se muestran mejor mediante CScript en lugar de WScript.

Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) para obtener ejemplos adicionales de scripting. En el caso de utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




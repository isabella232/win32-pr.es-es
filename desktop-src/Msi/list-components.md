---
description: El WiCompon.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo se puede usar para enumerar los componentes de una base de datos de Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Enumerar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809926"
---
# <a name="list-components"></a>Enumerar componentes

El WiCompon.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo se puede usar para enumerar los componentes de una base de datos de Windows Installer.

Este ejemplo muestra el uso de la clave principal en la [tabla de componentes](component-table.md).

En el ejemplo también se muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), el [**Método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md).
-   El [**método OpenView**](database-openview.md), la [**propiedad TablePersistent**](database-tablepersistent.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del [**objeto Database**](database-object.md).
-   El [**método Execute**](view-execute.md) y el [**método fetch**](view-fetch.md) del [**objeto View**](view-object.md).
-   Propiedad de [**propiedad StringData**](record-stringdata.md) del [**objeto de registro**](record-object.md).

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiCompon.vbs \[ ruta de acceso al \] \[ nombre de componente de base de datos\]**

Especifique la ruta de acceso a la base de datos Windows Installer. Especifique el nombre del componente. El nombre debe aparecer en la columna componente de la [tabla componente](component-table.md). Si se omite el nombre del componente, se muestran todos los componentes. Si se usa un asterisco ( \* ) como nombre del componente, WiCompon.vbs muestra la composición de todos los componentes. Tenga en cuenta que las bases de datos de gran tamaño se muestran mejor mediante CScript en lugar de WScript.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




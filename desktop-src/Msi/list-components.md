---
description: El archivo VBScript WiCompon.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. Este script de ejemplo se puede usar para enumerar los componentes de una base de Windows installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Enumerar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071963"
---
# <a name="list-components"></a>Enumerar componentes

El archivo VBScript WiCompon.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo se puede usar para enumerar los componentes de una base de Windows installer.

En este ejemplo se muestra el uso de la clave principal en la [tabla Component](component-table.md).

En el ejemplo también se muestra lo siguiente:

-   [**Método OpenDatabase (objeto installer),**](installer-opendatabase.md) [**el método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md).
-   [**Método OpenView**](database-openview.md), [**la propiedad TablePersistent**](database-tablepersistent.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del objeto [**Database**](database-object.md).
-   [**Método Execute**](view-execute.md) y [**el método Fetch**](view-fetch.md) del objeto [**View**](view-object.md).
-   [**Propiedad StringData**](record-stringdata.md) del objeto [**Record**](record-object.md).

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiCompon.vbs cscript \[ al nombre del componente de base de \] \[ datos\]**

Especifique la ruta de acceso a la base Windows del instalador. Especifique el nombre del componente. El nombre debe aparecer en la columna Componente de la [tabla Componente](component-table.md). Si se omite el nombre del componente, se enumeran todos los componentes. Si se usa un asterisco ( ) como nombre del \* componente, WiCompon.vbs enumera la composición de todos los componentes. Tenga en cuenta que las bases de datos grandes se muestran mejor con CScript en lugar de con WScript.

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador.](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, vea Windows Herramientas de desarrollo [del instalador .](windows-installer-development-tools.md)

 

 




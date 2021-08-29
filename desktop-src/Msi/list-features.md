---
description: El archivo VBScript WiFeatur.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Enumerar características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ace52bcbd4f2f456de5bc4dcbddc6b169e468d309190af0965dfe19304b05a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810985"
---
# <a name="list-features"></a>Enumerar características

El archivo VBScript WiFeatur.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se usa el script para enumerar las características de una base de datos Windows installer. En este ejemplo se muestra cómo agregar columnas temporales a una base de datos del Windows de solo lectura.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer),**](installer-opendatabase.md) [**el método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método Execute**](view-execute.md) y [**el método Fetch**](view-fetch.md) del objeto [**View**](view-object.md)
-   [**Método OpenView**](database-openview.md), la [**propiedad TablePersistent**](database-tablepersistent.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del objeto [**Database**](database-object.md)
-   [**Propiedad FieldCount**](record-fieldcount.md), [**propiedad IntegerData**](record-integerdata.md)y la [**propiedad StringData**](record-stringdata.md) del [**objeto Record**](record-object.md)

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiFeatur.vbs cscript \[ al nombre de la característica de base de \] \[ datos\]**

Especifique la ruta de acceso a la Windows del instalador. Especifique el nombre de la característica. Debe aparecer en la columna Característica de la [tabla Característica](feature-table.md). Si se omite el nombre de la característica, todas las características se muestran como un árbol de características. Si se usa un asterisco ( ) como nombre de \* característica, WiFeatur.vbs enumera la composición de todas las características. Tenga en cuenta que las bases de datos grandes se muestran mejor con CScript en lugar de con WScript.

Para obtener más información, vea [Windows de scripting del instalador para](windows-installer-scripting-examples.md) obtener ejemplos de scripting adicionales. Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




---
description: El archivo VBScript WiRunSQL.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Ejecutar SQL instrucciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7893da9c49ad1aaff4d19726cbcfce86f80293d9ffaa4c8e01569dd83a2d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044495"
---
# <a name="execute-sql-statements"></a>Ejecutar SQL instrucciones

El archivo VBScript WiRunSQL.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se usa el script para ejecutar SQL consultas y actualizaciones en una base de datos Windows Installer. Para obtener más información, [vea Sintaxis SQL y](sql-syntax.md) Ejemplos de consultas de base de datos mediante SQL y [script](examples-of-database-queries-using-sql-and-script.md).

El script de ejemplo muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y [**el método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)y el [**método Commit del**](database-commit.md) objeto [**Database**](database-object.md)
-   [**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del objeto [ **Record**](record-object.md)

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiRunSQL.vbs cscript \[ a consultas de SQL base de \] \[ datos\]**

Especifique la ruta de acceso a una base de Windows instalador. Especifique las SQL que se van a ejecutar. Tenga en cuenta que SQL consulta debe incluirse entre comillas dobles. Las consultas SELECT muestran las filas de la lista de resultados especificada en la consulta. No se muestran las columnas de datos binarios seleccionadas por una consulta.

Para obtener ejemplos de scripting adicionales, [Windows Ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de](windows-installer-development-tools.md)desarrollo del instalador .

Para obtener más información, vea [Trabajar con consultas y](working-with-queries.md) ejemplos de consultas de base de datos mediante SQL y [script](examples-of-database-queries-using-sql-and-script.md). En el [ejemplo A Localization Example (Ejemplo](a-localization-example.md) de localización) se muestra SQL [para](localizing-database-columns.md) la localización de columnas de base de datos y la actualización de una secuencia de información [de resumen](updating-a-summary-information-stream.md).

 

 




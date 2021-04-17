---
description: El WiRunSQL.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Ejecutar instrucciones SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652573"
---
# <a name="execute-sql-statements"></a>Ejecutar instrucciones SQL

El WiRunSQL.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se utiliza el script para ejecutar consultas SQL y actualizaciones en una base de datos de Windows Installer. Para obtener más información, vea [sintaxis SQL](sql-syntax.md) y [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).

El script de ejemplo muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)y el [**método commit**](database-commit.md) del [**objeto Database**](database-object.md)
-   [**Método Execute**](view-execute.md) del [ **objeto View**](view-object.md)
-   Propiedad de la [**propiedad StringData**](record-stringdata.md) del [ **objeto registro**](record-object.md)

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiRunSQL.vbs \[ ruta de acceso a \] \[ las consultas SQL de la base de datos\]**

Especifique la ruta de acceso a una base de datos de Windows Installer. Especifique las consultas SQL que se van a ejecutar. Tenga en cuenta que la consulta SQL se debe incluir entre comillas dobles. Las consultas SELECT muestran las filas de la lista de resultados especificada en la consulta. No se muestran las columnas de datos binarias seleccionadas por una consulta.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

Para obtener más información, vea [trabajar con consultas](working-with-queries.md) y [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md). En el ejemplo de [localización de ejemplo](a-localization-example.md) se muestra cómo usar SQL para [localizar columnas de base de datos](localizing-database-columns.md) y [actualizar un flujo de información de Resumen](updating-a-summary-information-stream.md).

 

 




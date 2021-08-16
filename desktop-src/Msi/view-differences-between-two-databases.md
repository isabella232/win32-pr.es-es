---
description: El archivo VBScript WiDiffDb.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. Este script de ejemplo genera un archivo de transformación temporal entre dos Windows del instalador y muestra la transformación.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Ver diferencias entre dos bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375918"
---
# <a name="view-differences-between-two-databases"></a>Ver diferencias entre dos bases de datos

El archivo VBScript WiDiffDb.vbs se proporciona en el [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo genera un archivo de transformación temporal entre dos Windows del instalador y muestra la transformación.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md)
-   [**Método GenerateTransform**](database-generatetransform.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Objeto de base de datos**](database-object.md)
-   [**Método Fetch**](view-fetch.md) del [ **objeto View**](view-object.md)
-   [**Propiedad IsNull**](record-isnull.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto Record**](record-object.md)
-   [\_Tabla TransformView](-transformview-table.md)

El uso de este ejemplo requiere la CScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiDiffDb.vbscscript** *\[ a la ruta de acceso de la base de datos original \] \[ a la base de datos revisada \]*

Especifique la ruta de acceso a la base de datos Windows instalador original. Especifique la ruta de acceso a la base de datos revisada. El script de ejemplo mostrará la transformación.

Para obtener ejemplos de scripting adicionales, [Windows Ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de](windows-installer-development-tools.md)desarrollo del instalador .

 

 




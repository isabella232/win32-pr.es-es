---
description: El WiDiffDb.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo genera un archivo de transformación temporal entre dos bases de datos de Windows Installer y muestra la transformación.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Ver las diferencias entre dos bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541190"
---
# <a name="view-differences-between-two-databases"></a>Ver las diferencias entre dos bases de datos

El WiDiffDb.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo genera un archivo de transformación temporal entre dos bases de datos de Windows Installer y muestra la transformación.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md)
-   [**Método GenerateTransform**](database-generatetransform.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Objeto de base de datos**](database-object.md)
-   [**Método fetch**](view-fetch.md) del [ **objeto View**](view-object.md)
-   [**Propiedad IsNull**](record-isnull.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)
-   [\_Tabla TransformView](-transformview-table.md)

El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiDiffDb.vbs** ruta de acceso de la base de datos *\[ original \] \[ a la base de datos \] revisada*

Especifique la ruta de acceso a la base de datos de Windows Installer original. Especifique la ruta de acceso a la base de datos revisada. El script de ejemplo mostrará la transformación.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




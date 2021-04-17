---
description: El WiMerge.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo combina una Windows Installer base de datos en otra base de datos. Para obtener más información, vea combinaciones y transformaciones.
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Fusión mediante combinación de dos bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653040"
---
# <a name="merge-two-databases"></a>Fusión mediante combinación de dos bases de datos

El WiMerge.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo combina una Windows Installer base de datos en otra base de datos. Para obtener más información, vea [combinaciones y transformaciones](merges-and-transforms.md).

La función [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) y el método [**Merge**](database-merge.md) del objeto [**Database**](database-object.md) no se pueden usar para combinar un módulo incluido en el paquete de instalación. No se deben usar para fusionar mediante combinación [módulos de combinación](merge-modules.md) en un paquete de Windows Installer. Para incluir un módulo de combinación en un paquete de instalación, los autores de paquetes de instalación deben seguir las instrucciones que se describen en el tema [aplicar módulos de combinación](applying-merge-modules.md) .

En el ejemplo se muestra el uso de lo siguiente:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Merge (método)**](database-merge.md)
-   [**Método commit**](database-commit.md) del [ **objeto Database**](database-object.md)
-   [**Fetch (método)**](view-fetch.md)
-   [**Objeto de vista**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto record**](record-object.md)

Para usar este ejemplo, debe tener la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiMerge.vbs \[ ruta de acceso de la base \] \[ de datos al \] \[ nombre de tabla de base de datos importada\]**

Especifique la ruta de acceso a la base de datos de Windows Installer que está recibiendo la combinación. Especifique la ruta de acceso a la base de datos que se va a importar en la primera. Puede especificar un nombre opcional para que una tabla contenga los errores de combinación. Si no se especifica ningún nombre de tabla, el instalador usa el nombre \_ MergeErrors y quita la tabla después de mostrar el contenido.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




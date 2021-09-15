---
description: El archivo VBScript WiMerge.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones. Este script de ejemplo combina una base de Windows installer en otra base de datos. Para obtener más información, vea Merges and Transforms( Mezclas y transformaciones).
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Combinar dos bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473973"
---
# <a name="merge-two-databases"></a>Combinar dos bases de datos

El archivo vbscript WiMerge.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) Este script de ejemplo combina una base de Windows installer en otra base de datos. Para obtener más información, [vea Merges and Transforms](merges-and-transforms.md).

La [**función MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) y el [**método Merge**](database-merge.md) del objeto [**Database**](database-object.md) no se pueden usar para combinar un módulo incluido en el paquete de instalación. No deben usarse para combinar módulos [de mezcla](merge-modules.md) en un paquete Windows Installer. Para incluir un módulo de mezcla en un paquete de instalación, los autores de paquetes de instalación deben seguir las instrucciones que se describen en [el tema Aplicar módulos de mezcla.](applying-merge-modules.md)

En el ejemplo se muestra el uso de lo siguiente:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md)
-   [**Método Merge**](database-merge.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md)
-   [**Ver objeto**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del [ **objeto Record**](record-object.md)

Debe tener la versión CScript.exe o WScript.exe del host Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiMerge.vbs cscript a \[ la ruta de acceso de la base de datos al nombre de la tabla de \] \[ base de \] \[ datos importada\]**

Especifique la ruta de acceso a la Windows del instalador que recibe la combinación. Especifique la ruta de acceso a la base de datos que se va a importar en la primera. Puede especificar un nombre opcional para una tabla que contiene los errores de combinación. Si no se especifica ningún nombre de tabla, el instalador usa el nombre MergeErrors y quita \_ la tabla después de mostrar el contenido.

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




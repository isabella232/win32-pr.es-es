---
description: El WiLstScr.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo muestra el visor de scripts de Windows Installer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Ver script del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677521"
---
# <a name="view-installer-script"></a>Ver script del instalador

El WiLstScr.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo muestra el visor de scripts de Windows Installer.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   Método [**LastErrorRecord**](installer-lasterrorrecord.md) del objeto [**Installer**](installer-object.md)
-   Método [**OpenView**](database-openview.md) del objeto [**Database**](database-object.md)
-   Método [**Fetch**](view-fetch.md) del objeto [**View**](view-object.md)
-   Método [**FormatText**](record-formattext.md)
-   Propiedad [**FieldCount**](record-fieldcount.md)
-   Propiedad [**StringData**](record-stringdata.md) del objeto [**Record**](record-object.md)
-   [\_Tabla TransformView](-transformview-table.md)

El uso de este ejemplo requiere la versión CScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiLstScr.vbs** *\[ ruta de acceso a Windows Installer \] script de ejecución*

Especifique la ruta de acceso al script de ejecución del instalador.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




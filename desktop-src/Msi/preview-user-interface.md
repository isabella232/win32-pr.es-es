---
description: El WiDialog.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se utiliza el script para obtener una vista previa de los cuadros de diálogo en una base de datos de Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Vista previa de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652741"
---
# <a name="preview-user-interface"></a>Vista previa de la interfaz de usuario

El WiDialog.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se utiliza el script para obtener una vista previa de los cuadros de diálogo en una base de datos de Windows Installer.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), el [**Método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md) y el [**método EnableUIpreview**](database-enableuipreview.md) del [**objeto Database**](database-object.md)
-   [**Método Execute**](view-execute.md) y [**método fetch**](view-fetch.md) del [**objeto View**](view-object.md)
-   Propiedad de la [**propiedad StringData**](record-stringdata.md) del [ **objeto registro**](record-object.md)

Este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiDialog.vbs** *\[ ruta de acceso a \] \[ los \] nombres de diálogo de base de datos*

Especifique la ruta de acceso a una base de datos de Windows Installer. Especifique el nombre de un cuadro de diálogo. Este nombre debe aparecer en la columna cuadro de diálogo de la [tabla del cuadro de diálogo](dialog-table.md). Para ver una cartelera, Anexe el nombre del cuadro de diálogo con el nombre del control de la [tabla de control](control-table.md) y anexe al nombre de la cartelera en la tabla de la [cartelera](billboard-table.md). Si no se especifica ningún cuadro de diálogo, todos los diálogos de la tabla de cuadro de diálogo se muestran secuencialmente.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




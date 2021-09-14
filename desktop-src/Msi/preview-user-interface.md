---
description: El archivo vbscript WiDialog.vbs se proporciona en los componentes del SDK de Windows para Windows instalador de aplicaciones. En este ejemplo se muestra cómo se usa el script para obtener una vista previa de los diálogos de una base de Windows installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Versión preliminar Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161452"
---
# <a name="preview-user-interface"></a>Versión preliminar Interfaz de usuario

El archivo vbscript WiDialog.vbs se proporciona en los componentes del SDK Windows [para desarrolladores Windows Installer](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se usa el script para obtener una vista previa de los diálogos de una base de Windows installer.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer),**](installer-opendatabase.md) [**el método CreateRecord**](installer-createrecord.md)y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md) y [**el método EnableUIpreview**](database-enableuipreview.md) del objeto [**Database**](database-object.md)
-   [**Método Execute**](view-execute.md) y [**el método Fetch**](view-fetch.md) del objeto [**View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) del objeto [ **Record**](record-object.md)

Este ejemplo requiere la versión CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiDialog.vbscscript a** *\[ los nombres de cuadro de diálogo \] \[ de base de datos \]*

Especifique la ruta de acceso a una base de Windows installer. Especifique el nombre de un cuadro de diálogo. Este nombre debe aparecer en la columna Diálogo de la [tabla Dialog](dialog-table.md). Para ver un cuadro de diálogo, anexe el nombre del cuadro de diálogo con el nombre del control de la [tabla Control](control-table.md) y anexe este al nombre de la publicidad en la [tabla Desc.](billboard-table.md) Si no se especifica ningún diálogo, todos los diálogos de la tabla Dialog se muestran secuencialmente.

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




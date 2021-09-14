---
description: El archivo VBScript WiUseXfm.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones. En este ejemplo se muestra cómo se puede usar el script para aplicar una transformación a una base de datos Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159130"
---
# <a name="apply-a-transform"></a>Aplicar una transformación

El archivo vbscript WiUseXfm.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo se puede usar el script para aplicar una transformación a una base de datos Windows Installer.

En el ejemplo se muestra el uso de

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método ApplyTransform**](database-applytransform.md)
-   [**Método Commit**](database-commit.md) del objeto [ **Database**](database-object.md)

Necesitará la versión CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiUseXfm.vbs cscript \[ a la ruta de acceso de la base de datos original para transformar las opciones de \] \[ \] \[ archivo\]**

Especifique la ruta de acceso a la base Windows instalador. Especifique la ruta de acceso al archivo de transformación. Si se omite la ruta de acceso al archivo de transformación, solo se comparan las dos bases de datos. El tercer argumento es un valor numérico opcional que especifica un conjunto de condiciones de error que se van a suprimir. Agregue estos valores juntos para suprimir varias condiciones.



| Value | Condición de error que se debe suprimir                   |
|-------|-----------------------------------------------|
| 1     | Agregar una fila que ya existe.             |
| 2     | Eliminar una fila que no existe.           |
| 4     | Agregar una tabla que ya existe.           |
| 8     | Eliminar una tabla que no existe.         |
| 16    | Actualizar una fila que no existe.           |
| 256   | No coincide con las páginas de códigos de base de datos y de transformación. |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




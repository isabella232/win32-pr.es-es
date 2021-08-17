---
description: El archivo VBScript WiLstScr.vbs se proporciona en los componentes del SDK de Windows para desarrolladores Windows Installer. Este script de ejemplo muestra el visor Windows script del instalador.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Ver script del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803986"
---
# <a name="view-installer-script"></a>Ver script del instalador

El archivo vbscript WiLstScr.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) Este script de ejemplo muestra el visor Windows script del instalador.

En el ejemplo se muestra el uso de:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md) del objeto [**Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md) del [**objeto View**](view-object.md)
-   [**Método FormatText**](record-formattext.md)
-   [**Propiedad FieldCount**](record-fieldcount.md)
-   [**Propiedad StringData**](record-stringdata.md) del [**objeto Record**](record-object.md)
-   [\_Tabla TransformView](-transformview-table.md)

El uso de este ejemplo requiere la CScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiLstScr.vbscscript** *\[ a Windows \] script de ejecución del instalador*

Especifique la ruta de acceso al script de ejecución del instalador.

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




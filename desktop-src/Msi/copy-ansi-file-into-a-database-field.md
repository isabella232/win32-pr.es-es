---
description: El archivo de ejemplo de código de VBScript WiTextIn.vbs se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copiar archivo ANSI en un campo de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667676"
---
# <a name="copy-ansi-file-into-a-database-field"></a>Copiar archivo ANSI en un campo de base de datos

El archivo de ejemplo de código de VBScript WiTextIn.vbs se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). En el ejemplo se muestra cómo se puede utilizar un script para copiar un archivo en un campo de texto de una base de datos de Windows Installer y se muestra el procesamiento de los datos de la clave principal.

En el ejemplo de código también se muestran los siguientes elementos:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md), [**método commit**](database-commit.md)y la [**propiedad PrimaryKeys**](database-primarykeys.md) del [**objeto Database**](database-object.md)
-   [**Método fetch**](view-fetch.md) y el [**método Modify**](view-modify.md) del [**objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) y [**método ReadStream**](record-readstream.md) del [**objeto record**](record-object.md)

Para usar el ejemplo de código, necesita la versión CScript.exe o WScript.exe de Windows Script Host.

**Para usar CScript.exe para ejecutar este ejemplo**

-   En el símbolo del sistema, escriba la siguiente sintaxis:

    **cscript WiTextIn.vbs \[ ruta de acceso al nombre de tabla de la base de datos \] \[ \] \[ valores de clave principal \] \[ \] \[ ruta de acceso al archivo\]**

> [!Note]  
> La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos.

 

**Para redirigir la salida a un archivo**

-   Finalice la línea de comandos con lo siguiente: **VBS > \[ ruta de acceso al archivo \] . T**

> [!Note]  
> El ejemplo devuelve un valor de 0 (cero) para Success, 1 (uno) si se invoca la ayuda y 2 (dos) si se produce un error en el script.

 

En la lista siguiente se identifican los elementos que debe especificar:

-   Especifique la ruta de acceso a la base de datos Windows Installer.
-   Especifique el nombre de la tabla de base de datos.
-   Especifique todos los valores de clave principal de la fila, en orden, y concatenados con dos puntos.
-   Especifique un nombre de columna que no sea una columna de clave. Esta es la columna que desea que reciba los datos.
-   Especifique la ruta de acceso al archivo de texto que se va a copiar.

> [!Note]  
> Si se omite el último argumento, se muestra el valor actual del campo.

 

Para obtener más ejemplos de scripting, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




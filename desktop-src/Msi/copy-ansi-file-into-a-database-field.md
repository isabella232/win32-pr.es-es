---
description: El archivo de ejemplo de código VBScript WiTextIn.vbs se proporciona en los componentes del SDK de Windows para Windows desarrolladores del instalador.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copiar un archivo ANSI en un campo de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65f38425fac327abd8eddaf9183464355ae025bb209947c750d4e3414d9b917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631335"
---
# <a name="copy-ansi-file-into-a-database-field"></a>Copiar un archivo ANSI en un campo de base de datos

El archivo de ejemplo de código WiTextIn.vbs VBScript se proporciona en los componentes del SDK de Windows para [Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) En el ejemplo se muestra cómo se puede usar un script para copiar un archivo en un campo de texto de una base de datos de Windows Installer y se muestra el procesamiento de datos de clave principal.

El ejemplo de código también muestra lo siguiente:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y [**el método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método OpenView**](database-openview.md), [**el método Commit**](database-commit.md)y la propiedad [**PrimaryKeys**](database-primarykeys.md) del objeto [**Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md) y [**el método Modify**](view-modify.md) del objeto [**View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) y [**método ReadStream**](record-readstream.md) del [**objeto Record**](record-object.md)

Para usar el ejemplo de código, necesita la CScript.exe o WScript.exe de Windows host de script.

**Para usar CScript.exe para ejecutar este ejemplo**

-   En el símbolo del sistema, escriba la sintaxis siguiente:

    **Ruta de acceso WiTextIn.vbs de cscript a la ruta de acceso del nombre de la tabla de base de datos valores de clave principal ruta de \[ \] \[ acceso del nombre \] \[ de columna al \] \[ \] \[ archivo\]**

> [!Note]  
> Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos.

 

**Para redirigir la salida a un archivo**

-   Finalice la línea de comandos con lo siguiente: **VBS > \[ ruta de acceso al archivo \] . T**

> [!Note]  
> El ejemplo devuelve un valor de 0 (cero) para el éxito, 1 (uno) si se invoca la Ayuda y 2 (dos) si se produce un error en el script.

 

En la lista siguiente se identifican los elementos que debe especificar:

-   Especifique la ruta de acceso a la base Windows de datos del instalador.
-   Especifique el nombre de la tabla de base de datos.
-   Especifique todos los valores de clave principal para la fila, en orden, y concatenados con dos puntos.
-   Especifique un nombre de columna que no sea una columna de clave. Esta es la columna que desea recibir los datos.
-   Especifique la ruta de acceso al archivo de texto que se va a copiar.

> [!Note]  
> Si se omite el último argumento, se muestra el valor actual del campo.

 

Para obtener más ejemplos de scripting, [vea Windows ejemplos de scripting del instalador.](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren el host Windows script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




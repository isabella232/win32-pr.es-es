---
description: El WiFilVer.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de versión, tamaño e idioma del archivo.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Administrar versiones y tamaños de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810730"
---
# <a name="manage-file-sizes-and-versions"></a>Administrar versiones y tamaños de archivo

El WiFilVer.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de versión, tamaño e idioma del archivo.

El ejemplo también muestra Windows Installer acciones, cómo obtener acceso a una base de datos Windows Installer y el uso de lo siguiente:

-   Método [**Installer. OpenDatabase**](installer-opendatabase.md) del [ **objeto Installer**](installer-object.md)
-   [**Installer. FileAttributes**](installer-fileattributes.md) (propiedad)
-   [**Instalador. FileHash**](installer-filehash.md) (método)
-   [**Installer. fileversion**](installer-fileversion.md) (método)
-   Método [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Database. OpenView**](database-openview.md) (método)
-   Propiedad [**Database. SummaryInformation**](database-summaryinformation.md) del [ **objeto Database**](database-object.md)
-   [**Session. OnAction**](session-doaction.md) (método)
-   [**Session. Property**](session-session.md)
-   [**Session. SourcePath**](session-sourcepath.md) (propiedad)
-   Propiedad [**Session. Mode**](session-mode.md) del [ **objeto Session**](session-object.md)
-   Propiedad [**Record. StringData**](record-stringdata.md)
-   Propiedad [**Record. IntegerData**](record-integerdata.md) del [ **objeto record**](record-object.md)

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema mediante la siguiente sintaxis:

**cscript WiFilVer.vbs \[ ruta de acceso a \] \[ ubicaciones de origen opcionales de base de datos\]**

Tenga en cuenta también lo siguiente:

-   La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos.
-   Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .
-   El ejemplo devuelve un valor de 0 (cero) para Success, 1 (uno) si se invoca la ayuda y 2 (dos) si se produce un error en el script.

Especifique el Windows Installer base de datos que desea actualizar, que debe estar ubicado en la raíz del archivo de origen. Sin embargo, puede especificar orígenes para la base de datos en ubicaciones independientes. Si el origen está comprimido, todos los archivos se abren en la raíz.

Las siguientes opciones se pueden especificar en cualquier ubicación de la línea de comandos.



| Opción                | Descripción                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *no se ha especificado ninguna opción* | Mostrar la información de archivo de la base de datos.                                            |
| /U                    | Actualice el tamaño del archivo, la versión y la información de idioma en la base de datos desde el origen. |



 

Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) y herramientas de desarrollo de [Windows Installer](windows-installer-development-tools.md).

 

 




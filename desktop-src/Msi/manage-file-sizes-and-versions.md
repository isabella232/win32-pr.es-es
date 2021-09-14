---
description: El archivo VBScript WiFilVer.vbs se proporciona en los componentes del SDK de Windows para Windows Instalador de aplicaciones. En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de idioma, el tamaño y la versión del archivo.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Administrar tamaños y versiones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074408"
---
# <a name="manage-file-sizes-and-versions"></a>Administrar tamaños y versiones de archivos

El archivo vbscript WiFilVer.vbs se proporciona en los componentes del SDK Windows [para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md) En el ejemplo se muestra cómo puede usar un script para notificar o actualizar la información de idioma, el tamaño y la versión del archivo.

En el ejemplo también se Windows acciones del instalador, cómo acceder a una base de datos Windows Installer y el uso de lo siguiente:

-   [**Método Installer.OpenDatabase**](installer-opendatabase.md) del [ **objeto Installer**](installer-object.md)
-   [**Installer.FileAttributes, propiedad**](installer-fileattributes.md)
-   [**Installer.FileHash (método)**](installer-filehash.md)
-   [**Installer.FileVersion (método)**](installer-fileversion.md)
-   [**Método Installer.LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)
-   [**Método Database.OpenView**](database-openview.md)
-   [**Propiedad Database.SummaryInformation**](database-summaryinformation.md) del objeto [ **Database**](database-object.md)
-   [**Método Session.DoAction**](session-doaction.md)
-   [**Session.Property**](session-session.md)
-   [**Propiedad Session.SourcePath**](session-sourcepath.md)
-   [**Propiedad Session.Mode**](session-mode.md) del [ **objeto Session**](session-object.md)
-   [**Propiedad Record.StringData**](record-stringdata.md)
-   [**Propiedad Record.IntegerData**](record-integerdata.md) del [ **objeto Record**](record-object.md)

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema mediante la sintaxis siguiente:

**Ruta de acceso WiFilVer.vbs cscript \[ a ubicaciones de origen \] \[ opcionales de base de datos\]**

Tenga en cuenta también lo siguiente:

-   Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos.
-   Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .
-   El ejemplo devuelve un valor de 0 (cero) para correcto, 1 (uno) si se invoca ayuda y 2 (dos) si se produce un error en el script.

Especifique la Windows del instalador que desea actualizar, que debe encontrarse en la raíz del archivo de origen. Sin embargo, puede especificar orígenes para la base de datos en ubicaciones independientes. Si el origen está comprimido, todos los archivos se abren en la raíz.

Las siguientes opciones se pueden especificar en cualquier ubicación de la línea de comandos.



| Opción                | Descripción                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *no se ha especificado ninguna opción* | Muestra la información de archivo de la base de datos.                                            |
| /U                    | Actualice el tamaño del archivo, la versión y la información de idioma de la base de datos desde el origen. |



 

Para obtener más información, vea [Windows ejemplos de scripting del instalador y](windows-installer-scripting-examples.md) Windows herramientas de desarrollo del instalador [.](windows-installer-development-tools.md)

 

 




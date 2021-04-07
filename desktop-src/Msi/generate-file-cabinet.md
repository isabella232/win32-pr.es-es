---
description: El WiMakCab.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. En este ejemplo se muestra cómo se usa el script para generar archivadores de archivos a partir de una base de datos de Windows Installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Generar archivo. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df2355c247ff602d644d2865ec3b9d9a8447ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002265"
---
# <a name="generate-file-cabinet"></a>Generar archivo. cab

El WiMakCab.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se usa el script para generar archivadores de archivos a partir de una base de datos de Windows Installer.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y el [**método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método commit**](database-commit.md), el [**método OpenView**](database-openview.md) y la [**propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md) del [**objeto Database**](database-object.md)
-   [**Método fetch**](view-fetch.md), método [**Execute**](view-execute.md) y [**método Modify**](view-modify.md) del [**objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) y [**propiedad IntegerData**](record-integerdata.md) del [**objeto record**](record-object.md)
-   [**Método OnAction**](session-doaction.md), [**propiedad Property (objeto Session)**](session-session.md)y la [**propiedad Mode**](session-mode.md) del [**objeto Session**](session-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiMakCab.vbs \[ ruta de acceso a \] \[ las \] \[ ubicaciones de origen opcionales de nombre base de base de datos\]**

Para generar un archivo. cab, Makecab.exe debe estar en la ruta de acceso. La utilidad de Makecab.exe se incluye en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Tenga en cuenta que el ejemplo no actualiza la [tabla de medios](media-table.md) para controlar varios gabinetes. Para reemplazar un archivo. cab incrustado, incluya las opciones:/R/C/U/E.

Especifique la ruta de acceso a la base de datos del instalador. Debe estar ubicado en la raíz del árbol de origen. Especifique el nombre base que distingue entre mayúsculas y minúsculas para los archivos. cab generados. Si el tipo de origen está comprimido, se abren todos los archivos en la raíz. Se pueden especificar las siguientes opciones en cualquier punto de la línea de comandos.



| Opción              | Descripción                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción |                                                                                                                                           |
| /C                  | Ejecute la compresión. Si no se especifica/C, WiMakCab.vbs solo genera el archivo DDF.                                                        |
| /L                  | Use la compresión LZX en lugar de MSZIP                                                                                                      |
| /F                  | Limite el tamaño de los contenedores a un tamaño de disquete de 1,44 MB en lugar de a un CD-ROM                                                                              |
| /U                  | Actualizar la base de datos para hacer referencia al archivo. cab generado                                                                                    |
| /E                  | Insertar el archivo. cab en el paquete del instalador como una secuencia                                                                               |
| /S                  | Usar números de secuencia en la tabla de archivos ordenados por directorios                                                                             |
| /R                  | Revertir a una instalación que no sea de archivador. Quite Cabinet si se especifica/E (la opción/R quita la propiedad bit comprimido-SummaryInfo 15 & 2) |



 

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




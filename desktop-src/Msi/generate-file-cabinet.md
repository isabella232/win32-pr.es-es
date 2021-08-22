---
description: El archivo VBScript WiMakCab.vbs se proporciona en los componentes Windows SDK para desarrolladores Windows Installer. En este ejemplo se muestra cómo se usa el script para generar archivadores de archivos a partir de una base de Windows installer.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Generar archivador de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581504"
---
# <a name="generate-file-cabinet"></a>Generar archivador de archivos

El archivo vbscript WiMakCab.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) En este ejemplo se muestra cómo se usa el script para generar archivadores de archivos a partir de una base de Windows installer.

En este ejemplo se muestra:

-   [**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) y [**el método LastErrorRecord**](installer-lasterrorrecord.md) del [**objeto Installer**](installer-object.md)
-   [**Método Commit**](database-commit.md), el [**método OpenView y**](database-openview.md) la propiedad [**SummaryInformation (objeto Database)**](database-summaryinformation.md) del objeto [**Database**](database-object.md)
-   [**Método Fetch**](view-fetch.md), [**Execute y**](view-execute.md) Modify [**del**](view-modify.md) [**objeto View**](view-object.md)
-   [**Propiedad StringData**](record-stringdata.md) y [**propiedad IntegerData**](record-integerdata.md) del [**objeto Record**](record-object.md)
-   [**Método DoAction**](session-doaction.md), la [**propiedad Property (objeto Session)**](session-session.md)y la [**propiedad Mode**](session-mode.md) del objeto [**Session**](session-object.md)

Necesitará la versión CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe para ejecutar este ejemplo, escriba un comando en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiados argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiMakCab.vbs cscript a \[ ubicaciones de \] \[ origen opcionales de nombre base de base de \] \[ datos\]**

Para generar un gabinete, Makecab.exe debe estar en path. La utilidad Makecab.exe se incluye en los componentes del [SDK de Windows para Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Tenga en cuenta que el ejemplo no actualiza la [tabla Media para](media-table.md) controlar varios gabinetes. Para reemplazar un gabinete incrustado, incluya las opciones: /R /C /U /E.

Especifique la ruta de acceso a la base de datos del instalador. Debe encontrarse en la raíz del árbol de origen. Especifique el nombre base que distingue mayúsculas de minúsculas para los archivos de archivado generados. Si el tipo de origen está comprimido, todos los archivos se abren en la raíz. Las siguientes opciones se pueden especificar en cualquier punto de la línea de comandos.



| Opción              | Descripción                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| no se ha especificado ninguna opción |                                                                                                                                           |
| /C                  | Ejecute la compresión. Si no se especifica /C, WiMakCab.vbs solo genera el archivo DDF.                                                        |
| /L                  | Uso de la compresión LZX en lugar de MSZIP                                                                                                      |
| /F                  | Limitar el tamaño del gabinete a un tamaño de disquete de 1,44 MB en lugar de CD-ROM                                                                              |
| /U                  | Actualización de la base de datos para hacer referencia al gabinete generado                                                                                    |
| /E                  | Inserción del archivo contenedor en el paquete del instalador como una secuencia                                                                               |
| /S                  | Uso de números de secuencia en la tabla File ordenada por directorios                                                                             |
| /R                  | Revertir a la instalación que no es de gabinete, quitar el gabinete si se especifica /E (la opción /R quita el bit comprimido: la propiedad SummaryInfo 15 & 2) |



 

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




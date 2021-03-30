---
description: El WiGenXfm.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este script de ejemplo puede generar una transformación de dos bases de datos Windows Installer. Para obtener más información, vea transformaciones de base de datos.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815214"
---
# <a name="generate-a-transform"></a>Generar una transformación

El WiGenXfm.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo puede generar una transformación de dos bases de datos Windows Installer. Para obtener más información, vea [transformaciones de base de datos](database-transforms.md).

En el ejemplo se muestra el uso de:

[**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)

[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)

[**Método GenerateTransform**](database-generatetransform.md) del [ **objeto Database**](database-object.md)

Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiGenXfm.vbs \[ ruta de acceso de la base de datos original a la ruta de acceso de la \] \[ base de datos revisada \] \[\]**

Especifique la ruta de acceso a la base de datos de Windows Installer original. Especifique la ruta de acceso a la base de datos revisada. Especifique la ruta de acceso al archivo de transformación que se va a crear. Si se omite la ruta de acceso al archivo de transformación, las dos bases de datos solo se comparan.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

Tenga en cuenta que [un ejemplo de localización](a-localization-example.md) muestra [la generación de una transformación de personalización](generating-a-customization-transform.md).

 

 




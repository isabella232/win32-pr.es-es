---
description: El archivo VBScript WiGenXfm.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. Este script de ejemplo puede generar una transformación a partir de dos bases de Windows installer. Para obtener más información, vea Transformaciones de base de datos.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074747"
---
# <a name="generate-a-transform"></a>Generar una transformación

El archivo VBScript WiGenXfm.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo puede generar una transformación a partir de dos bases de Windows installer. Para obtener más información, vea [Transformaciones de base de datos](database-transforms.md).

En el ejemplo se muestra el uso de:

[**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md)

[**Método LastErrorRecord**](installer-lasterrorrecord.md) del [ **objeto Installer**](installer-object.md)

[**Método GenerateTransform**](database-generatetransform.md) del objeto [ **Database**](database-object.md)

Necesitará la versión de CScript.exe o WScript.exe de Windows script para usar este ejemplo. Para usar CScript.exe ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiGenXfm.vbs cscript a la ruta de acceso de la base de datos \[ original a la ruta de acceso de base de datos revisada para transformar el \] \[ \] \[ archivo\]**

Especifique la ruta de acceso a la base de datos Windows instalador original. Especifique la ruta de acceso a la base de datos revisada. Especifique la ruta de acceso al archivo de transformación que se va a crear. Si se omite la ruta de acceso al archivo de transformación, solo se comparan las dos bases de datos.

Para obtener ejemplos de scripting adicionales, [vea Windows ejemplos de scripting del instalador.](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, vea Windows Herramientas de desarrollo [del instalador .](windows-installer-development-tools.md)

Tenga en [cuenta que un ejemplo de localización](a-localization-example.md) muestra la [generación de una transformación de personalización](generating-a-customization-transform.md).

 

 




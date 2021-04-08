---
description: El WiToAnsi.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se utiliza el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar un archivo Unicode en un archivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910710"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiar un archivo Unicode en un archivo ANSI

El WiToAnsi.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este ejemplo muestra cómo se utiliza el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.

El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis. La ayuda se muestra si el primer argumento es/? o si se especifican pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**cscript WiToAnsi.vbs \[ ruta de acceso a la ruta de acceso del archivo Unicode \] \[ al archivo ANSI\]**

Especifique el archivo de texto Unicode que se va a convertir. Especifique el archivo de texto ANSI que se va a crear. Si no se especifica ningún archivo ANSI, se reemplaza el archivo Unicode.

Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md). En el caso de utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).

 

 




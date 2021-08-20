---
description: El archivo VBScript WiToAnsi.vbs se proporciona en los componentes del SDK de Windows para Windows instaladores. En este ejemplo se muestra cómo se usa el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar un archivo Unicode en un archivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224a9115da67848bd43aaceb7e5d8f529693558191e52a04de2e7645a4e60aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143379"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiar un archivo Unicode en un archivo ANSI

El archivo VBScript WiToAnsi.vbs se proporciona en los componentes del SDK de Windows [para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). En este ejemplo se muestra cómo se usa el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.

El uso de este ejemplo requiere la CScript.exe o WScript.exe de Windows host de script. Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la sintaxis siguiente. Se muestra ayuda si el primer argumento es /? o si se especifican demasiado pocos argumentos. Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] . El ejemplo devuelve un valor de 0 para correcto, 1 si se invoca la ayuda y 2 si se produce un error en el script.

**Ruta de acceso WiToAnsi.vbs cscript \[ a la ruta de acceso del archivo Unicode al archivo \] \[ ANSI\]**

Especifique el archivo de texto Unicode que se va a convertir. Especifique el archivo de texto ANSI que se va a crear. Si no se especifica ningún archivo ANSI, se reemplaza el archivo Unicode.

Para obtener ejemplos de scripting adicionales, [Windows Ejemplos de scripting del instalador de .](windows-installer-scripting-examples.md) Para obtener utilidades de ejemplo que no requieren Windows host de script, [vea Windows Herramientas de desarrollo del instalador .](windows-installer-development-tools.md)

 

 




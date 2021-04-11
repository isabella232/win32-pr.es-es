---
description: MSITool. Mak es un archivo make que se puede usar para compilar herramientas y acciones personalizadas.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: MSITool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156153"
---
# <a name="msitoolmak"></a>MSITool. Mak

MSITool. Mak es un archivo make que se puede usar para compilar herramientas y acciones personalizadas. Se puede usar con Visual C++ versión 4,0 o posterior. Para obtener más información, vea el archivo de encabezado. Requiere que se defina un conjunto de valores antes de incluir este archivo. Normalmente, los desarrolladores colocan al principio de. cpp, ifdef que se omitirá en el compilador de C. Del mismo modo, los recursos se agregan al final del archivo. cpp. Vea los ejemplos para obtener más información.

VCBIN se puede definir en el directorio donde se encuentran las herramientas de Visual C++ o el archivo make usa MSVCDIR y MSDEVDIR. Si no están definidas, no especifica ninguna ubicación, suponiendo que las herramientas estén en la ruta de acceso. Un problema con las variables de entorno en Visual C++ versión 5,0 es que si ambos no están en su ruta de acceso, el enlazador no puede encontrar Msdis100.dll. Si lo copia de MSDEVDIR a MSVCDIR, funcionará. La otra opción es copiar Msdis100.dll y Rc.exe y Rcdll.dll en MSVCDIR, y establecer VCBIN en ese.

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




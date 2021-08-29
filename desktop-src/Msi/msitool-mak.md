---
description: Msitool.mak es un archivo Make que puede usar para compilar herramientas y acciones personalizadas.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool.mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86392153c539dfab771b8e87859147ef89573e0aa9747771593674e99262e6c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944412"
---
# <a name="msitoolmak"></a>Msitool.mak

Msitool.mak es un archivo Make que puede usar para compilar herramientas y acciones personalizadas. Se puede usar con Visual C++ versión 4.0 o posterior. Para obtener más información, vea el archivo de encabezado. Requiere que se defina un conjunto de valores antes de incluir este archivo. Normalmente, los desarrolladores los ponen al principio del archivo .cpp, ifdef que el compilador de C debe omitir. Del mismo modo, se agregan recursos al final del archivo .cpp. Consulte ejemplos para obtener más información.

VCBIN se puede definir en el directorio donde se encuentran las herramientas Visual C++ o el archivo make usa MSVCDIR y MSDEVDIR. Si no se definen, no especifica una ubicación, suponiendo que las herramientas estén en path. Un problema con las variables de entorno de Visual C++ versión 5.0 es que, si ambos no están en la ruta de acceso, el vinculador no puede encontrar Msdis100.dll. Si lo copia de MSDEVDIR a MSVCDIR, funciona. La otra opción es copiar Msdis100.dll y Rc.exe y Rcdll.dll en MSVCDIR y establecer VCBIN en eso.

Esta herramienta solo está disponible en los componentes del [SDK Windows para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




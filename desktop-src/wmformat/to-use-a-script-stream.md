---
title: Para usar una secuencia de script
description: Para usar una secuencia de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- secuencias de scripts, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357742"
---
# <a name="to-use-a-script-stream"></a>Para usar una secuencia de script

En esta sección se describe cómo enviar datos de script al escritor para incluirlos en un archivo. Para obtener información sobre cómo incluir secuencias de scripts en perfiles, vea [configuración de tipos de secuencia arbitrarios](configuring-arbitrary-stream-types.md).

Cada script consta de dos cadenas: una cadena de *tipo* y una cadena de *argumento* .

Se debe dar formato a los datos del script antes de que se envíen al escritor. Las cadenas se deben concatenar, separarse mediante un carácter **nulo** y terminar con un carácter **nulo** . En el ejemplo siguiente se muestra un script legítimo:



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | \\0 | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | \\0 |



 

Cada par de comandos de script debe escribirse como un ejemplo en el escritor. Para obtener más información sobre cómo escribir ejemplos, consulte [para escribir ejemplos](to-write-samples.md).

Cuando se reproduzca el archivo ASF, el lector (o lector sincrónico) entregará los comandos de script en el orden temporal de la presentación. Es responsabilidad de la aplicación analizar las dos cadenas y responder al comando de script.

> [!Note]  
> Al usar DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar comandos de script**](using-script-commands.md)
</dt> </dl>

 

 





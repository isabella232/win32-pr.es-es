---
title: Para usar una secuencia de scripts
description: Para usar una secuencia de scripts
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows SDK de formato multimedia, secuencias de script
- Formato de sistemas avanzados (ASF), secuencias de script
- ASF (formato de sistemas avanzados), secuencias de script
- secuencias de script, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d8df991ae97cc6d9eb330f11cb8798f5f2eb2787b5947e1d997b3d276d15f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929215"
---
# <a name="to-use-a-script-stream"></a>Para usar una secuencia de scripts

En esta sección se describe cómo enviar datos de script al escritor para su inclusión en un archivo. Para obtener información sobre cómo incluir secuencias de script en perfiles, vea [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).

Cada script consta de dos cadenas, una *cadena de tipo* y una cadena de *argumento.*

Los datos del script deben tener formato antes de enviarse al escritor. Las cadenas se deben concatenar, separar por un **carácter NULL** y terminar con un **carácter** NULL. En el ejemplo siguiente se muestra un script legítimo:



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

Cada par de comandos de script debe escribirse como un ejemplo para el escritor. Para obtener más información sobre cómo escribir ejemplos, vea [Para escribir ejemplos.](to-write-samples.md)

Cuando se reproduce el archivo ASF, el lector (o lector sincrónico) entregará los comandos de script en el orden de tiempo de presentación. Es responsabilidad de la aplicación analizar las dos cadenas y responder al comando de script.

> [!Note]  
> Cuando se usa DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de comandos de script**](using-script-commands.md)
</dt> </dl>

 

 





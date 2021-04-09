---
title: Comando de archivo de respuesta
description: Un archivo de respuesta es un archivo de texto que contiene una o más opciones de la línea de comandos del compilador de MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referencia de la línea de comandos MIDL, comando de archivo de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994476"
---
# <a name="the-response-file-command"></a>Comando de archivo de respuesta

Un archivo de respuesta es un archivo de texto que contiene una o más opciones de la línea de comandos del compilador de MIDL. A diferencia de la línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo. Esto puede ser útil debido a las limitaciones del entorno de compilación o como una comodidad para el proceso de compilación.

## <a name="switch-options"></a>Opciones de conmutador

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*archivo de respuesta \_*
</dt> <dd>

Especifica el nombre de un archivo de respuesta. El nombre del archivo de respuesta debe seguir inmediatamente al carácter @. No se permite ningún espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Como alternativa a colocar todas las opciones asociadas con un modificador en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos. Las opciones de un archivo de respuesta se interpretan como si estuvieran presentes en esa ubicación en la línea de comandos de MIDL.

Cada argumento de un archivo de respuesta debe comenzar y finalizar en la misma línea. El carácter de barra diagonal inversa ( \) no se puede usar para concatenar líneas. Cuando forma parte de una cadena entrecomillada en el archivo de respuesta, el carácter de barra diagonal inversa solo se puede usar antes de otra barra diagonal inversa o antes de un carácter de comilla doble ("). Cuando no forma parte de una cadena entrecomillada, el carácter de barra diagonal inversa solo se puede usar antes de un carácter de comillas dobles.

MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta combinados con otros modificadores de la línea de comandos.

El compilador MIDL no admite archivos de respuesta anidados.

## <a name="examples"></a>Ejemplos

**MIDL @midl.rsp**

**MIDL-Oicf @midl1.rsp -env Win32 @midl2.rsp ITF. idl**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





---
title: El comando archivo de respuesta
description: Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referencia de la línea de comandos MIDL, comando de archivo de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c40d8f4255b15a7b95b9bdca9e72ae2cba8e7ea1d42281f441326090a9529d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013533"
---
# <a name="the-response-file-command"></a>El comando archivo de respuesta

Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL. A diferencia de una línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo. Esto puede ser útil debido a las limitaciones del entorno de compilación o por comodidad para el proceso de compilación.

## <a name="switch-options"></a>Opciones de cambio

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*archivo de \_ respuesta*
</dt> <dd>

Especifica el nombre de un archivo de respuesta. El nombre del archivo de respuesta debe seguir inmediatamente el carácter @. No se permite ningún espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Como alternativa a colocar todas las opciones asociadas a un modificador en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos. Las opciones de un archivo de respuesta se interpretan como si se encuentran en esa ubicación en la línea de comandos de MIDL.

Cada argumento de un archivo de respuesta debe comenzar y terminar en la misma línea. El carácter de barra diagonal inversa ( \\ ) no se puede usar para concatenar líneas. Cuando forma parte de una cadena entrecomillada en el archivo de respuesta, el carácter de barra diagonal inversa solo se puede usar antes de otra barra diagonal inversa o antes de un carácter de comilla doble ("). Cuando no forma parte de una cadena entre comillas, el carácter de barra diagonal inversa solo se puede usar antes de un carácter de comilla doble.

MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta combinados con otros modificadores de línea de comandos.

El compilador MIDL no admite archivos de respuesta anidados.

## <a name="examples"></a>Ejemplos

**Midl @midl.rsp**

**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





---
title: El comando de archivo de respuesta
description: Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referencia de línea de comandos MIDL, comando de archivo de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387671"
---
# <a name="the-response-file-command"></a>El comando de archivo de respuesta

Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL. A diferencia de una línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo. Esto puede ser útil debido a las limitaciones del entorno de compilación o para su proceso de compilación.

## <a name="switch-options"></a>Cambiar opciones

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*archivo \_ de respuesta*
</dt> <dd>

Especifica el nombre de un archivo de respuesta. El nombre del archivo de respuesta debe seguir inmediatamente el carácter @. No se permite ningún espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Como alternativa a colocar todas las opciones asociadas a un modificador en la línea de comandos, el compilador midl acepta archivos de respuesta que contienen modificadores y argumentos. Las opciones de un archivo de respuesta se interpretan como si se encuentran en esa ubicación en la línea de comandos de MIDL.

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

 

 





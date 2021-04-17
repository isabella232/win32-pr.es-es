---
title: Formatos de mensajes de error y ADVERTENCIA
description: Lista de formatos de mensajes de advertencia y mensajes de error de MIDL.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- errores MIDL, formatos de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42552b8106b72d82b2b13b69a7cba7ac2e99e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419097"
---
# <a name="error-and-warning-message-formats"></a>Formatos de mensajes de error y ADVERTENCIA

Los errores de la línea de comandos aparecen en el siguiente formato:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

El campo de información de error adicional proporciona información específica del contexto en función del mensaje de error. Por ejemplo, cuando se produce un error de declaración de tipo sin resolver, el campo de información de error adicional muestra el nombre del tipo que no se pudo resolver.

Las advertencias en tiempo de compilación aparecen en el formato siguiente:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Los errores en tiempo de compilación aparecen en el siguiente formato:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

La información de contexto opcional hace referencia al contexto en el que se produjo el error. Se genera cuando el compilador MIDL detecta un error durante el análisis semántico de las firmas de tipo y procedimiento. El compilador MIDL notifica esta información para ayudarle a encontrar el error en el archivo IDL rápidamente.

Los mensajes de error del sistema aparecen en el siguiente formato:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Este mensaje se genera debido a un error inesperado. El número de error hexadecimal es un identificador de error del sistema de Windows XP, Windows 2000, Windows NT, Windows 98 o Windows 95. Puede encontrar información adicional en Winerror. h o NTSTATUS. h. Para obtener más información sobre cómo resolver las condiciones que causaron este error, vea el texto de error para el [error del compilador](compiler-errors.md) MIDL9008.

 

 





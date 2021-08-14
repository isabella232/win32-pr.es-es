---
title: Formatos de mensaje de error y advertencia
description: Lista de formatos de mensaje de error y mensaje de advertencia de MIDL.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- errores MIDL, formatos de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384421"
---
# <a name="error-and-warning-message-formats"></a>Formatos de mensaje de error y advertencia

Los errores de línea de comandos aparecen en el formato siguiente:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

El campo información de error adicional proporciona información específica del contexto en función del mensaje de error. Por ejemplo, cuando se produce un error de declaración de tipo sin resolver, el campo información de error adicional muestra el nombre del tipo que no se pudo resolver.

Las advertencias en tiempo de compilación aparecen en el formato siguiente:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Los errores en tiempo de compilación aparecen en el formato siguiente:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

La información de contexto opcional hace referencia al contexto en el que se produjo el error. Se genera cuando el compilador MIDL detecta un error durante el análisis semántico de firmas de tipo y procedimiento. El compilador MIDL informa de esta información para ayudarle a encontrar rápidamente el error en el archivo IDL.

Los mensajes de error del sistema aparecen en el formato siguiente:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Este mensaje se genera mediante un error inesperado. El número de error hexadecimal es un identificador de error del sistema Windows XP, Windows 2000, Windows NT, Windows 98 o Windows 95. Puede encontrar información adicional en Winerror.h o Ntstatus.h. Para obtener más información sobre cómo trabajar en torno a las condiciones que provocaron este error, vea el texto del error del [compilador](compiler-errors.md) MIDL9008.

 

 





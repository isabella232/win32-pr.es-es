---
description: Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que entienden algunos de los reconocedores de escritura a mano de Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referencia de sintaxis de expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574448"
---
# <a name="regular-expression-syntax-reference"></a>Referencia de sintaxis de expresiones regulares

Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que entienden algunos de los reconocedores de escritura a mano de Microsoft. La sintaxis es un subconjunto de la implementación [del lenguaje de expresiones](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) regulares en el .NET Framework.

Hay algunas diferencias en la forma en que se usan las expresiones regulares de escritura a mano y la forma en que se usan los otros tipos de expresiones regulares. La sintaxis de escritura a mano se usa para especificar una cadena exacta que coincidirá con el motor de reconocimiento y no con una subcadena. Por ejemplo, la expresión regular s( \[ a-z +)p devolvería \] coincidencias para "la comida", "stop", "instep" y "esophagus". Mientras que una expresión regular de escritura a mano equivalente, como s(!IS \_ ONECHAR)+p, coincidiría con la "comida" y la "detenerse", pero no con "instep" y "esophagus".

Las expresiones regulares de escritura a mano no admiten espacios sin separación dentro de las expresiones regulares. Es decir, no se puede usar la entidad "nbsp" dentro de una expresión regular de escritura a mano.

En las secciones siguientes se describe la sintaxis con más detalle.

## <a name="valid-operators"></a>Operadores válidos

Los operadores siguientes son válidos para crear expresiones regulares para definir ámbitos de entrada para reconocedores de escritura a mano.



| Operator      | Descripción                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Operador unario postfijo que significa cero o más apariciones del operando.<br/> |
| +<br/>  | Operador unario postfijo que significa una o varias apariciones del operando.<br/>  |
| ?<br/>  | Operador unario postfijo que significa cero o una aparición del operando.<br/>   |
| \|<br/> | Operador de infijo binario que significa "o".<br/>                                        |
| ()<br/> | Se usa para agrupar elementos.<br/>                                                       |



 

La implementación de Microsoft de expresiones regulares para reconocedores de escritura a mano permite aplicaciones repetidas de operadores unarios postfijos. Por ejemplo, a \* \* = (a \* ) = a , \* \* b?? = (b?)? = b?. También permiten repeticiones no consecutivas, por ejemplo: ? \* \* = ((a \* )?) \* = (a ) = a \* \* \* . Esto es diferente de .NET Framework expresiones regulares, que solo permiten ? operador que se va a repetir.

Otra diferencia de .NET Framework expresiones regulares es que la escritura a mano de expresiones regulares no admite una expresión vacía designada con un par vacío de paréntesis, ().

> [!Note]  
> Solo se admiten caracteres en la página de códigos 1252 para escribir expresiones regulares a mano.

 

## <a name="using-input-scopes"></a>Uso de ámbitos de entrada

También puede usar el conjunto de ámbitos de entrada normales que se definen como parte de la [**función SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) en las expresiones regulares. Por ejemplo, el valor de Month (numérico) es IS \_ DATE \_ MONTH. La sintaxis para especificar un ámbito de entrada como parte de una expresión regular es anteponer el valor enumerado del ámbito de entrada con un paréntesis abierto y un signo de exclamación, (!, y colocar un paréntesis de cierre, ), al final. Por ejemplo:

(!IS \_ DATE \_ MONTH)

Si combina el ámbito de entrada IS DEFAULT mediante ORing con cualquier otro ámbito de entrada, el efecto es que el reconocedor puede devolver cualquier expresión única que admita el modelo de lenguaje predeterminado (por ejemplo, una palabra del diccionario del sistema o una fecha) con o sin signo de puntuación, o cualquier valor que cumpla el resto de la expresión regular pasada al \_ reconocedor.

> [!Note]  
> Los siguientes miembros de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) no se admiten en expresiones regulares: IS \_ PHRASELIST, IS \_ REGULAREXPRESSION, IS \_ SRGS, IS \_ XML.

 

## <a name="unsupported-operators"></a>Operadores no admitidos

No se admiten los siguientes operadores de expresión regular al crear expresiones regulares de escritura a mano.



| Operator                                     | Descripción                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Carácter de punto.<br/>                                        |
| \[\]<br/>                              | Corchetes. Use paréntesis para agrupar elementos.<br/>     |
| {}<br/>                                | Llaves.<br/>                                          |
| (?\# comment) y \# \[ comment\]<br/> | Comentarios.<br/>                                                |
| $<br/>                                 | Carácter de signo de dólar.<br/>                                   |
| ^<br/>                                 | Carácter de carácter de caret.<br/>                                         |
| -<br/>                                 | Carácter de guion. Debe or ( \| ) juntos todos los conjuntos de elementos.<br/> |



 

## <a name="escaping-characters"></a>Evitar caracteres

Los caracteres normales, distintos de los de la tabla siguiente, coinciden entre sí. Es decir, una "a" en una expresión regular especifica que la entrada debe coincidir con una "a".

Otra diferencia significativa en la escritura de expresiones regulares de escritura a mano es que solo se puede escapar un conjunto limitado de caracteres dentro de una expresión regular. En la tabla siguiente se describe el conjunto permitido de caracteres que se pueden escapar. Cualquier otro intento de escape de un carácter producirá un error por parte del reconocedor.



| Carácter       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 
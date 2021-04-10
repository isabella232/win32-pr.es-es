---
description: Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que comprenden algunos de los reconocedores de escritura a mano de Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referencia de sintaxis de expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279739"
---
# <a name="regular-expression-syntax-reference"></a>Referencia de sintaxis de expresiones regulares

Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que comprenden algunos de los reconocedores de escritura a mano de Microsoft. La sintaxis es un subconjunto de la [implementación del lenguaje de expresiones regulares](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) en el .NET Framework.

Hay algunas diferencias en la forma en que se usan las expresiones regulares de escritura a mano y en la forma en que se usan los otros tipos de expresiones regulares. La sintaxis de escritura a mano se usa para especificar una cadena exacta que coincidirá con el motor de reconocimiento y no con una subcadena. Por ejemplo, las expresiones regulares s ( \[ a-z \] +) p devolverán coincidencias para "sopa", "STOP", "inStep" y "esophagus". Mientras que una expresión regular de escritura a mano equivalente, como s (! IS \_ ONECHAR) + p, coincidiría con "sopa" y "STOP", pero no con "inStep" y "esophagus".

Las expresiones regulares de escritura a mano no admiten espacios de no separación dentro de expresiones regulares. Es decir, no puede usar la entidad "nbsp" dentro de una expresión regular de escritura a mano.

En las secciones siguientes se describe la sintaxis con más detalle.

## <a name="valid-operators"></a>Operadores válidos

Los operadores siguientes son válidos para crear expresiones regulares para definir ámbitos de entrada para reconocedores de escritura a mano.



| Operator      | Descripción                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Operador unario de postfijo que indica cero o más repeticiones del operando.<br/> |
| +<br/>  | Operador unario postfijo que indica una o más repeticiones del operando.<br/>  |
| ?<br/>  | Operador unario de postfijo que indica cero o una repetición del operando.<br/>   |
| \|<br/> | Significado del operador binario de infijo "or".<br/>                                        |
| ()<br/> | Se utiliza para agrupar elementos.<br/>                                                       |



 

La implementación de Microsoft de expresiones regulares para reconocedores de escritura a mano permite aplicaciones repetidas de operadores unarios de postfijo. Por ejemplo, a \* \* = (a \* ) \* = a \* , b?? = (b?)? = b?. También permiten repeticiones no consecutivas, por ejemplo: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* . Esto es diferente de .NET Framework expresiones regulares, que solo permiten el? operador que se va a repetir.

Otra diferencia de .NET Framework expresiones regulares es que las expresiones regulares de escritura a mano no admiten una expresión vacía designada con un par de paréntesis vacío, ().

> [!Note]  
> Solo se admiten caracteres en la página de códigos 1252 para las expresiones regulares de escritura a mano.

 

## <a name="using-input-scopes"></a>Usar ámbitos de entrada

También puede usar el conjunto de ámbitos de entrada normales que se definen como parte de la función [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) en las expresiones regulares. Por ejemplo, el valor de month (numérica) es \_ Date \_ month. La sintaxis para especificar un ámbito de entrada como parte de una expresión regular es anteponer el valor enumerado del ámbito de entrada con un paréntesis de apertura y un signo de exclamación, (! y colocar un paréntesis de cierre,) al final. Por ejemplo:

(! Es \_ mes de la fecha \_ )

Si combina el ámbito de \_ entrada predeterminado de is oring con cualquier otro ámbito de entrada, el efecto es que el reconocedor puede devolver cualquier expresión única que admita el modelo de lenguaje predeterminado (por ejemplo, una palabra del Diccionario del sistema o una fecha) con o sin puntuación, o cualquier valor que cumpla el resto de la expresión regular pasada al reconocedor.

> [!Note]  
> Los siguientes miembros de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) no se admiten en expresiones regulares: is \_ PHRASELIST, is REGULAREXPRESSION, IS \_ \_ SRGS, is \_ xml.

 

## <a name="unsupported-operators"></a>Operadores no admitidos

No se admiten los siguientes operadores de expresión regular al crear expresiones regulares de escritura a mano.



| Operator                                     | Descripción                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Carácter de punto.<br/>                                        |
| \[\]<br/>                              | Corchetes. Use paréntesis para agrupar elementos.<br/>     |
| {}<br/>                                | Llaves.<br/>                                          |
| (?\# comentario) y \# \[ Comentario\]<br/> | Comentarios.<br/>                                                |
| $<br/>                                 | Carácter de signo de dólar.<br/>                                   |
| ^<br/>                                 | Carácter de intercalación.<br/>                                         |
| -<br/>                                 | Carácter de guión. Debe o ( \| ) juntos todos los conjuntos de elementos.<br/> |



 

## <a name="escaping-characters"></a>Evitar caracteres

Los caracteres ordinarios, excepto los de la tabla siguiente, coinciden. Es decir, una "a" en una expresión regular especifica que la entrada debe coincidir con una "a".

Otra diferencia significativa en la escritura de expresiones regulares de escritura a mano es que solo puede escapar un conjunto limitado de caracteres dentro de una expresión regular. En la tabla siguiente se describe el conjunto de caracteres permitido que se puede usar como carácter de escape. Cualquier otro intento de escapar un carácter producirá un error producido por el reconocedor.



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



 

 

 
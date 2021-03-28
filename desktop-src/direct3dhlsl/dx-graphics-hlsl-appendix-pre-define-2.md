---
title: '\#define (Directiva) (macro)'
description: Directiva de preprocesador que crea una macro similar a una función.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104997005"
---
# <a name="define-directive-macro"></a>\#define (Directiva) (macro)

Directiva de preprocesador que crea una macro similar a una función.



| \#define el *identificador*( *argument0*,..., *argumentn-1* ) *token-String* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*<br/>                                                                                                                                                                             | Identificador de la macro. <br/> Una segunda [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para una macro con un identificador que ya existe en el contexto actual genera un error a menos que la segunda secuencia del token sea idéntica a la primera. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentn-1* ) <br/> | Lista de argumentos de la macro. La lista de argumentos está delimitada por comas, puede tener cualquier longitud y debe incluirse entre paréntesis. Cada nombre de argumento de la lista debe ser único. Ningún espacio en blanco puede separar el parámetro de *identificador* y el paréntesis de apertura. <br/> Usar concatenación de línea Coloque una barra diagonal inversa ( \) inmediatamente antes del carácter de nueva línea para dividir las directivas largas en varias líneas de código fuente. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-cadena* \[ opta\] <br/>                                                                                                                     | Valor de la macro. Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas. Uno o más caracteres de espacio en blanco deben separar este parámetro del parámetro *Identifier* ; Este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto. Haga un uso liberal de los paréntesis para asegurarse de que los argumentos complicados se interpreten correctamente. <br/> Si el valor del parámetro *Identifier* aparece dentro del parámetro *token-String* (incluso como resultado de otra expansión de macro), no se expande. <br/> Si excluye este parámetro, todas las instancias del parámetro *Identifier* se quitan del archivo de código fuente. El identificador permanece definido y se puede probar mediante las directivas [ \# If Defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef y \# ifndef. <br/> |



 

## <a name="remarks"></a>Observaciones

Todas las instancias del parámetro de *identificador* que se producen después de la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de código fuente constituyen una llamada de macro y el identificador se reemplazará por una versión del parámetro de *cadena de token* que tenga argumentos reales sustituidos por parámetros formales. El número de parámetros de la llamada debe coincidir con el número de parámetros de la definición de macro. El identificador solo se reemplaza cuando forma un token. por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.

La directiva [ \# UNDEF](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# UNDEF (Directiva) (DirectX HLSL).

La definición de constantes con la opción/D del compilador tiene el mismo efecto que el uso de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo. Se pueden definir hasta 30 macros con la opción/D.

Los argumentos reales de la llamada de macro coinciden con los argumentos formales correspondientes en la definición de macro. Cada argumento formal de la cadena de token se reemplaza por el argumento real correspondiente, a menos que el argumento esté precedido por un operador de generación de cadenas ( \# ), de carácter ( \# @) o de pegado de token ( \# \# ), o que vaya seguido de un \# \# operador. Cualquier macro en el argumento real se expande antes de que la directiva reemplace el parámetro formal.

El pegado de tokens en el compilador de HLSL es ligeramente diferente del pegado de tokens en el compilador de C, en que los tokens pegados deben ser tokens válidos por su cuenta. Por ejemplo, considere la siguiente definición de macro:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



En el compilador de C, esto da como resultado lo siguiente:


```
float4x4 test
```



Sin embargo, en el compilador HLSL, esto da como resultado lo siguiente:


```
float4 x4 test
```



Puede solucionar este comportamiento mediante la siguiente definición de macro.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa una macro para definir líneas de cursores.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



En el ejemplo siguiente se define una macro que recupera un entero pseudoaleatorio en el intervalo especificado.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#UNDEF (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






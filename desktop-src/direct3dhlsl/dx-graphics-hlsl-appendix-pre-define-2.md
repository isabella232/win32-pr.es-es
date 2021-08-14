---
title: '\#define (directiva) (macro)'
description: Directiva de preprocesador que crea una macro de tipo función.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49f89847a47a173f8f7d3bcbb22464fecad658068031f62559bde6ec0735f7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514816"
---
# <a name="define-directive-macro"></a>\#define (directiva) (macro)

Directiva de preprocesador que crea una macro de tipo función.



| \#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/>                                                                                                                                                                             | Identificador de la macro. <br/> Una segunda [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) para una macro con un identificador que ya existe en el contexto actual genera un error a menos que la segunda secuencia de tokens sea idéntica a la primera. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* ) <br/> | Lista de argumentos de la macro. La lista de argumentos está delimitada por comas, puede tener cualquier longitud y debe ir entre paréntesis. Cada nombre de argumento de la lista debe ser único. Ningún espacio en blanco puede separar *el parámetro de identificador* y el paréntesis de apertura. <br/> Use la concatenación de líneas para colocar una barra diagonal inversa ( ) inmediatamente antes del carácter de nueva línea para dividir las directivas \\ largas en varias líneas de origen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Opcional\] <br/>                                                                                                                     | Valor de la macro. Este parámetro consta de una serie de tokens, como palabras clave, constantes o instrucciones completas. Uno o varios caracteres de espacio en blanco deben separar este parámetro del *parámetro identifier;* este espacio en blanco no se considera parte del texto sustituido, ni es ningún espacio en blanco después del último token del texto. Use paréntesis para asegurarse de que los argumentos complicados se interpretan correctamente. <br/> Si el valor del parámetro *identifier* se produce dentro del parámetro *token-string* (incluso como resultado de otra expansión de macro), no se expande. <br/> Si excluye este parámetro, todas las instancias del parámetro *identifier* se quitan del archivo de origen. El identificador permanece definido y se puede probar mediante las directivas [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md) \# , ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Comentarios

Todas las instancias del parámetro *identifier* que se producen después de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de origen constituyen una llamada macro y el identificador se reemplazará por una versión del parámetro *token-string* que tenga argumentos reales sustituidos por parámetros formales. El número de parámetros de la llamada debe coincidir con el número de parámetros de la definición de macro. El identificador solo se reemplaza cuando forma un token; Por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.

La [ \# directiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# Undef Directive (DirectX HLSL).

Definir constantes con la opción del compilador /D tiene el mismo efecto que usar la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo. Se pueden definir hasta 30 macros con la opción /D.

Los argumentos reales de la llamada macro coinciden con los argumentos formales correspondientes en la definición de macro. Cada argumento formal de la cadena de token se reemplaza por el argumento real correspondiente, a menos que el argumento esté precedido por un operador de cadena ( \# ), charizing ( @) o \# token-pasting ( \# \# ), \# o seguido de un \# operador . Cualquier macro en el argumento real se expande antes de que la directiva reemplace el parámetro formal.

La pega de tokens en el compilador HLSL es ligeramente diferente de la pegada de tokens en el compilador de C, ya que los tokens pegaron deben ser tokens válidos por sí mismos. Por ejemplo, considere la siguiente definición de macro:


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



Puede evitar este comportamiento mediante la siguiente definición de macro en su lugar.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa una macro para definir líneas de cursor.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



En el ejemplo siguiente se define una macro que recupera un entero pseudoaleativo en el intervalo especificado.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#directiva undef (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






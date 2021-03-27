---
title: '\#define (Directiva, Constant)'
description: Directiva de preprocesador que asigna un nombre descriptivo a una constante de la aplicación.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104077140"
---
# <a name="define-directive-constant"></a>\#define (Directiva, Constant)

Directiva de preprocesador que asigna un nombre descriptivo a una constante de la aplicación.



| \#definición *de identifiertoken: cadena* |
|-----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*<br/>                                          | Identificador de la constante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-cadena* \[ opta\]<br/> | Valor de la constante. Este parámetro se compone de una serie de tokens, como palabras clave, constantes o instrucciones completas. Uno o más caracteres de espacio en blanco deben separar este parámetro del parámetro *Identifier* ; Este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto. <br/> Si excluye este parámetro, todas las instancias del parámetro *Identifier* se quitan del archivo de código fuente. El identificador permanece definido y se puede probar mediante las directivas [ \# If Defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef y \# ifndef. <br/> |



 

## <a name="remarks"></a>Observaciones

Todas las instancias del parámetro de *identificador* que se producen después de la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de código fuente se reemplazarán por el valor del parámetro de *cadena de token* . El identificador solo se reemplaza cuando forma un token. por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.

La directiva [ \# UNDEF](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# UNDEF (Directiva) (DirectX HLSL).

La definición de constantes con la opción/D del compilador tiene el mismo efecto que el uso de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo. Se pueden definir hasta 30 constantes con la opción/D. Para obtener un ejemplo de cómo se puede usar, vea la sección ejemplos de [ \# ifdef y)](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define el ancho del identificador como la constante entera 80 y, a continuación, se define la longitud en términos de ancho y la constante de tipo entero 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Cada instancia subsiguiente de LENGTH se reemplaza por (WIDTH + 10) y cada instancia subsiguiente de WIDTH + 10 se reemplaza por la expresión (80 + 10). Los paréntesis alrededor del ancho + 10 son importantes porque controlan la interpretación en instrucciones como las siguientes.


```
var = LENGTH * 20;
```



Después de la fase de preprocesamiento, la instrucción pasa a ser la siguiente, que se evalúa como 1.800.


```
var = ( 80 + 10 ) * 20;
```



Sin paréntesis, el resultado sería el siguiente, que se evalúa como 280.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#UNDEF (Directiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






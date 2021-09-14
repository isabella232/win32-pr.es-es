---
title: '\#define (directiva) (constante)'
description: Directiva de preprocesador que asigna un nombre significativo a una constante de la aplicación.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974745"
---
# <a name="define-directive-constant"></a>\#define (directiva) (constante)

Directiva de preprocesador que asigna un nombre significativo a una constante de la aplicación.



| \#definir *identifiertoken-string* |
|-----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/>                                          | Identificador de la constante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[ Opcional\]<br/> | Valor de la constante. Este parámetro consta de una serie de tokens, como palabras clave, constantes o instrucciones completas. Uno o varios caracteres de espacio en blanco deben separar este parámetro del *parámetro identifier;* este espacio en blanco no se considera parte del texto sustituido, ni tampoco ningún espacio en blanco después del último token del texto. <br/> Si excluye este parámetro, todas las instancias del parámetro *identifier* se quitan del archivo de origen. El identificador permanece definido y se puede probar mediante las directivas [ \# ifdefined](dx-graphics-hlsl-appendix-pre-ifdef.md) \# , ifdef \# e ifndef. <br/> |



 

## <a name="remarks"></a>Observaciones

Todas las instancias del parámetro *identifier* que se producen después de la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) en el archivo de origen se reemplazarán por el valor del *parámetro token-string.* El identificador solo se reemplaza cuando forma un token; Por ejemplo, el identificador no se reemplaza si aparece en un comentario, dentro de una cadena o como parte de un identificador más largo.

La [ \# directiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocesador que olvide la definición de un identificador; para obtener más información, vea \# undef Directive (DirectX HLSL).

Definir constantes con la opción del compilador /D tiene el mismo efecto que usar la directiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) al principio del archivo. Se pueden definir hasta 30 constantes con la opción /D. Para obtener un ejemplo de cómo se puede usar, vea la sección Ejemplos de [ \# ifdef y ).](dx-graphics-hlsl-appendix-pre-ifdef.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define el identificador WIDTH como la constante de entero 80 y, a continuación, se define LENGTH en términos de WIDTH y la constante de entero 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Cada instancia posterior de LENGTH se reemplaza por (WIDTH + 10) y cada instancia posterior de WIDTH + 10 se reemplaza por la expresión (80 + 10). Los paréntesis alrededor de WIDTH + 10 son importantes porque controlan la interpretación en instrucciones como las siguientes.


```
var = LENGTH * 20;
```



Después de la fase de preprocesamiento, la instrucción se convierte en la siguiente, que se evalúa como 1800.


```
var = ( 80 + 10 ) * 20;
```



Sin paréntesis, el resultado sería el siguiente, que se evalúa como 280.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#directiva undef (HLSL de DirectX)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






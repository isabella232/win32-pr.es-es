---
title: packoffset
description: Palabra clave opcional de empaquetado constante de sombreador, que usa la sintaxis siguiente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826084"
---
# <a name="packoffset"></a>packoffset

Palabra clave opcional de empaquetado constante de sombreador, que usa la sintaxis siguiente:

: packoffset( c \[ Subcomponent \] \[ .component \] )



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                 | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Palabra clave required.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**C**<br/>                                                                                                                             | El empaquetado solo se aplica a los registros constantes (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent \] \[ .component\]**<br/> | Subcomponentes y componentes opcionales. Un subcomponente es un número de registro, que es un entero. Un componente tiene el formato \[ .xyzw \] .<br/> |



 

## <a name="remarks"></a>Comentarios

Use esta palabra clave para empaquetar manualmente una constante de sombreador [al declarar un tipo de variable](dx-graphics-hlsl-variable-syntax.md).

Al empaquetar una constante, no se pueden mezclar tipos constantes.

El compilador se comporta de forma ligeramente diferente para las constantes globales y las constantes uniformes:

-   Constante global. El compilador agrega una variable global como una constante global a *$Global* cbuffer. Los elementos empaquetados automáticamente (los declarados sin packoffset) aparecerán después de la última variable empaquetada manualmente. Puede mezclar tipos al empaquetar constantes globales.
-   Constante uniforme. El compilador agregará un parámetro uniforme en la lista de parámetros de una función $Param un búfer constante de *$Param* cuando el sombreador se compile fuera del marco de efectos. Cuando se compila dentro del marco de efectos, una constante uniforme debe resolverse en una variable uniforme definida en el ámbito global. Una constante uniforme no se puede desplazar manualmente; Su uso recomendado es solo para la especialización de sombreadores en los que se les aplica el alias de vuelta a los globales, no como un medio de pasar datos de aplicación al sombreador.

Estos son algunos ejemplos adicionales: [empaquetado de constantes mediante el modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Ejemplos

Estos son varios ejemplos de empaquetado manual de constantes de sombreador.

Empaquetar subcomponentes de vectores y escalares cuyo tamaño es lo suficientemente grande como para evitar cruzar los límites del registro. Por ejemplo, todos estos son válidos:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (HLSL de DirectX)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 






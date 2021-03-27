---
title: packoffset
description: Palabra clave de empaquetado constante de sombreador opcional, que usa la sintaxis siguiente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL de packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358080"
---
# <a name="packoffset"></a>packoffset

Palabra clave de empaquetado constante de sombreador opcional, que usa la siguiente sintaxis:



|                                                 |
|-------------------------------------------------|
| : packoffset ( \[ subcomponente de c \] \[ . Component \] ) |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                 | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Palabra clave required.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**unidad**<br/>                                                                                                                             | El empaquetado se aplica solo a los registros constantes (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[SubComponent \] \[ . Component\]**<br/> | Subcomponentes y componentes opcionales. Un subcomponente es un número de registro, que es un entero. Un componente tiene el formato \[ . xyzw \] .<br/> |



 

## <a name="remarks"></a>Observaciones

Use esta palabra clave para empaquetar manualmente una constante de sombreador al [declarar un tipo de variable](dx-graphics-hlsl-variable-syntax.md).

Cuando se empaqueta una constante, no se pueden mezclar tipos constantes.

El compilador se comporta de forma ligeramente diferente para las constantes globales y las constantes uniformes:

-   Constante global. Una variable global se agrega como una constante global a un *$global* CBuffer por el compilador. Los elementos empaquetados automáticamente (los declarados sin packoffset) aparecerán después de la última variable empaquetada manualmente. Puede mezclar tipos al empaquetar constantes globales.
-   Constante uniforme. El compilador *$param* agregará un parámetro uniforme en la lista de parámetros de una función cuando el sombreador se compile fuera del marco de trabajo de efectos. Cuando se compila dentro del marco de trabajo de efecto, una constante uniforme debe resolverse en una variable uniforme definida en el ámbito global. Una constante uniforme no puede desplazarse manualmente; su uso recomendado es solo para la especialización de los sombreadores en los que el alias se vuelve a globales, no como un medio para pasar datos de aplicación al sombreador.

Estos son algunos ejemplos adicionales: [empaquetar constantes con el modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Ejemplos

Estos son algunos ejemplos de cómo empaquetar manualmente las constantes de sombreador.

Empaquete subcomponentes de vectores y escalares cuyo tamaño sea lo suficientemente grande como para evitar cruzar los límites del registro. Por ejemplo, todos son válidos:


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

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 






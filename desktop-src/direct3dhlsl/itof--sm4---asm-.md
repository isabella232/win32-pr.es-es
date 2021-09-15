---
title: itof (sm4 - asm)
description: Conversión de entero con signo a punto flotante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569893"
---
# <a name="itof-sm4---asm"></a>itof (sm4 - asm)

Conversión de entero con signo a punto flotante.



| itof dest \[ .mask \] , \[ - \] src0 \[ .swzzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene el resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene el valor que se debe convertir.<br/>        |



 

## <a name="remarks"></a>Observaciones

Esta instrucción de conversión de entero a flotante con signo supone que *src0* contiene una tupla de 4-tupla de entero de 32 bits con signo. Una vez ejecutada la instrucción, *dest* contendrá una tupla de 4 puntos flotantes.

La conversión se realiza por componente.

Cuando un valor de entrada entero es demasiado grande en magnitud para representarse exactamente en el formato de punto flotante, se recomienda encarecidamente redondear al modo par más cercano, pero no es necesario.

El modificador negate opcional en el operando de origen toma el complemento de 2 antes de realizar la operación aritmética.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






---
title: itof (sm4 - asm)
description: Conversión de entero con signo a punto flotante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f473b5cc9664ee1c9acab88381bc9de6a5b4897fac3899923c6bb20c22bba7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986485"
---
# <a name="itof-sm4---asm"></a>itof (sm4 - asm)

Conversión de entero con signo a punto flotante.



| itof dest \[ .mask \] , \[ - \] src0 \[ .swzzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene el resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene el valor que se debe convertir.<br/>        |



 

## <a name="remarks"></a>Comentarios

En esta instrucción de conversión de entero a flotante con signo se da por supuesto que *src0* contiene una tupla de 4-tupla de entero de 32 bits con signo. Una vez ejecutada la instrucción, *dest* contendrá una tupla de 4 puntos flotantes.

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
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






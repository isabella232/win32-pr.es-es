---
title: ishl (sm4 - asm)
description: Mayús a la izquierda. | ishl (sm4 - asm)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbf71acbf137a63002ae87f2304140dfe26a863280dff98d1f260c87234a44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089382"
---
# <a name="ishl-sm4---asm"></a>ishl (sm4 - asm)

Mayús a la izquierda.



| dest \[ .mask \] , src0 \[ .swprendle, \] src1.select \_ component |
|---------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene los valores que se deben desplazar.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Contiene la cantidad de desplazamiento.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un desplazamiento por componente de cada valor de 32 bits en *src0* a la izquierda por un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en el componente *\_ src1.select,* insertando 0. Los resultados de 32 bits por componente se colocan *en dest*. El recuento es un valor escalar aplicado a todos los componentes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






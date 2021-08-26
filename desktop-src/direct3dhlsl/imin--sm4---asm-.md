---
title: imin (sm4 - asm)
description: Entero por componente mínimo.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0188b23700393034ad2187636d8d5bf846b8b8523b5336699443475c094fd26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982395"
---
# <a name="imin-sm4---asm"></a>imin (sm4 - asm)

Entero por componente mínimo.



| imin dest \[ .mask \] , \[  - \] src0 \[ .swzzle, \] \[ - \] src1 \[ .sw swzzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/> *dest*  =  *src0*  <  *src1* ? *src0:* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor que se va a comparar con *src1.*<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El valor que se va a comparar con *src0.*<br/>                                                       |



 

## <a name="remarks"></a>Comentarios

El modificador negate opcional en operandos de origen toma el complemento de 2 antes de realizar la operación.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






---
title: lt (sm4 - asm)
description: Comparación de punto flotante vectorial por componente menor que.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0e05a3a3f8d6ee540315ac44cd590c6561b47522f42fd510ec1439232387e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023775"
---
# <a name="lt-sm4---asm"></a>lt (sm4 - asm)

Comparación de punto flotante vectorial por componente menor que.



| lt dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swzzle, \] \[ - \] src1 abs \[ \_ \] \[ .swzzle\] |
|----------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor que se va a comparar con *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El valor que se va a comparar con *src0*.<br/>             |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza la comparación float (*src0*  <  *src1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es verdadera, 0xFFFFFFFF se devuelve para ese componente. En caso 0x0000000 se devuelve

Los desnormados se vacían antes de la comparación; los registros de origen originales no se han tocado.

+0 es igual a -0.

La comparación con NaN devuelve false.

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

 

 






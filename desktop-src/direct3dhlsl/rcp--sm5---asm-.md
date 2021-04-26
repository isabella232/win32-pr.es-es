---
title: rcp (sm5 - asm)
description: Recíproco por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998252"
---
# <a name="rcp-sm5---asm"></a>rcp (sm5 - asm)

Recíproco por componente.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados<br/> *dest*  =  **1.0f**  /  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El número del que se debe tomar el recíproco.<br/>                             |



 

## <a name="remarks"></a>Comentarios

Use esta instrucción para reducir la precisión mutua, independientemente de los requisitos estrictos para la división.

El error relativo máximo es 2-21. (La tolerancia a errores solo coincide con rsq)

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.



| *src*  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *Dest* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






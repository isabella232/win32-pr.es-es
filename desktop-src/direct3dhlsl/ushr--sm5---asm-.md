---
title: ushr (sm5 - asm)
description: Mayús a la derecha. | ushr (sm5 - asm)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063674"
---
# <a name="ushr-sm5---asm"></a>ushr (sm5 - asm)

Mayús a la derecha.



| yfe dest \[ \] .mask, src0 \[ .swprendle, \] src1 \[ .sw swle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene los resultados de la instrucción.<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los valores de 32 bits que se desplazarán.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] LSB 5 bits proporcionan el número de bits que se desplazarán (0-31).<br/> |



 

Esta instrucción realiza un desplazamiento por componente de cada valor de 32 bits en *src0* a la derecha por un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en *src1,* insertando 0. Los resultados de 32 bits por componente se colocan en *dest*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
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

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






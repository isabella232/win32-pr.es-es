---
title: ushr (SM5-ASM)
description: Desplazar a la derecha. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986503"
---
# <a name="ushr-sm5---asm"></a>ushr (SM5-ASM)

Desplazar a la derecha.



| ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] contiene los resultados de la instrucción.<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los valores de 32 bits que se van a desplazar.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los 5 bits de LSB, proporcione el número de bits que se van a desplazar (0-31).<br/> |



 

Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits de *src0* a la derecha un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) en *SRC1*, insertando 0. Los resultados de 32 bits por componente se colocan en *dest*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






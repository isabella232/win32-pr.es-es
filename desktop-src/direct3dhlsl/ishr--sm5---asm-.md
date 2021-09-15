---
title: ishr (sm5 - asm)
description: Desplazamiento aritmético a la derecha (extensión de signo). | ishr (sm5 - asm)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569300"
---
# <a name="ishr-sm5---asm"></a>ishr (sm5 - asm)

Desplazamiento aritmético a la derecha (extensión de signo).



| ishl dest \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene los resultados del desplazamiento.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El número de bits que se desplazarán.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los valores de 32 bits que se desplazarán.<br/>        |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un desplazamiento aritmético por componente de cada valor de 32 bits en *src0* justo por un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en *src1,* replicando el valor del bit 31. El resultado de 32 bits por componente se coloca en *dest*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






---
title: ige (sm4 - asm)
description: Comparación de enteros vectoriales por componente mayor o igual que.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15de044678d61adea52607166c622e6fb5dc20211499de4c11066e6688216910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982425"
---
# <a name="ige-sm4---asm"></a>ige (sm4 - asm)

Comparación de enteros vectoriales por componente mayor o igual que.



| ige dest \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente que se va a comparar con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El componente que se va a comparar con *src0*.<br/> |



 

## <a name="remarks"></a>Comentarios

Realiza la comparación de enteros (*src0*  >=  *src1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es verdadera, 0xFFFFFFFF se devuelve para ese componente. De lo 0x0000000 se devuelve .

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

 

 






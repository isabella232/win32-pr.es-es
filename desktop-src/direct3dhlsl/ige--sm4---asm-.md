---
title: ige (sm4 - asm)
description: Comparación de enteros vectoriales por componente mayor o igual que.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567781"
---
# <a name="ige-sm4---asm"></a>ige (sm4 - asm)

Comparación de enteros vectoriales por componente mayor o igual que.



| ige dest \[ .mask \] , src0 \[ .swzzle \] , src1 \[ .sw swle\] |
|-------------------------------------------------------|



 



| Elemento                                                            | Descripción                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente que se va a comparar con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El componente que se va a comparar con *src0*.<br/> |



 

## <a name="remarks"></a>Observaciones

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

 

 






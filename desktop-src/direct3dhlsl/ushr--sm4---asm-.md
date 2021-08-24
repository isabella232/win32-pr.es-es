---
title: ushr (sm4 - asm)
description: Mayús a la derecha. | ushr (sm4 - asm)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55343f9c9b4db4fff4b0df7ab4e2a567f25f0eb43e93486fe9c41b89cf68454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787825"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4 - asm)

Mayús a la derecha.



| ushr dest \[ .mask \] , src0 \[ .swzzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componentes que se desplazarán.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] La cantidad que se va a desplazar *src0*.<br/>                 |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un desplazamiento por componente de cada valor de 32 bits en *src0* a la derecha por un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en el componente *\_ src1.select,* insertando 0. El resultado de 32 bits por componente se coloca en *dest*. El recuento es un valor escalar aplicado a todos los componentes.

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

 

 






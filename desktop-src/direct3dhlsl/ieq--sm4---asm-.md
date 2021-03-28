---
title: iEQ (SM4-ASM)
description: Comparación de igualdad de entero de vector de modo de componente.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996953"
---
# <a name="ieq-sm4---asm"></a>iEQ (SM4-ASM)

Comparación de igualdad de entero de vector de modo de componente.



| dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|---------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor que se va a comparar con *SRC1*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el valor que se va a comparar con *src0*.<br/>           |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza la comparación de enteros (*src0*  ==  *SRC1*) para cada componente y escribe el resultado en *dest*.

Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente. De lo contrario, se devuelve 0x0000000

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






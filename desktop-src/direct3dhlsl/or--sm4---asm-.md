---
title: o (sm4 - asm)
description: Bit a bit o .
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568909"
---
# <a name="or-sm4---asm"></a>o (sm4 - asm)

Bit a bit o .



| o dest \[ .mask \] , src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|------------------------------------------------------|



 



| Elemento                                                            | Descripción                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/>      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes a OR con *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes a OR con *src0*.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un OR lógico por componente de cada par de valores de 32 bits de *src0* y *src1*. Los resultados de 32 bits se colocan en *dest*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






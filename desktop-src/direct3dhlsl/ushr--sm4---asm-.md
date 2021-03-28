---
title: ushr (SM4-ASM)
description: Desplazar a la derecha. | ushr (SM4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279978"
---
# <a name="ushr-sm4---asm"></a>ushr (SM4-ASM)

Desplazar a la derecha.



| ushr dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1. Select ( \_ componente) |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a desplazar.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] la cantidad que se va a desplazar *src0*.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits de *src0* a la derecha un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) de *SRC1. Seleccione el \_ componente*, insertando 0. El resultado de 32 bits por componente se coloca en el *destino*. El recuento es un valor escalar que se aplica a todos los componentes.

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

 

 






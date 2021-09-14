---
title: ushr (sm4 - asm)
description: Mayús a la derecha. | ushr (sm4 - asm)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063675"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4 - asm)

Mayús a la derecha.



| ushr dest \[ .mask \] , src0 \[ .swzzle \] , src1.select \_ (componente) |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componentes que se desplazarán.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] La cantidad que se va a desplazar *src0*.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits en *src0* a la derecha mediante un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en el componente *\_ src1.select,* insertando 0. El resultado de 32 bits por componente se coloca en *dest*. El recuento es un valor escalar aplicado a todos los componentes.

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

 

 






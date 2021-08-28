---
title: ishr (sm4 - asm)
description: Desplazamiento aritmético a la derecha (extensión de signo). | ishr (sm4 - asm)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2ec191320561b05ba736b7da5630fb50a610e739d0e74f9def3eaa10bb4e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511140"
---
# <a name="ishr-sm4---asm"></a>ishr (sm4 - asm)

Desplazamiento aritmético a la derecha (extensión de signo).



| ishr dest \[ .mask \] , src0 \[ .swzzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene el resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene el valor que se va a desplazar.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Contiene la cantidad de desplazamiento.<br/>            |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un desplazamiento aritmético por componente de cada valor de 32 bits en *src0* a la derecha mediante un recuento de bits enteros sin signo proporcionado por el LSB de 5 bits (intervalo 0-31) en el componente *\_ src1.select,* replicando el valor del bit 31. El resultado de 32 bits por componente se coloca en *dest*. El recuento es un valor escalar aplicado a todos los componentes.

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

 

 






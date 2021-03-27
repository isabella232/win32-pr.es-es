---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Compare y intercambie en memoria de inmediato.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904300"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a>IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)

Compare y intercambie en memoria de inmediato.



| IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . Single \_ Component \_ Mask \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select \_ Component \] , SRC1 \[ . Select \_ Component\] |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[out \] contiene *dst1* antes de la escritura.<br/>                                                                              |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[en \] una vista de acceso desordenado (UAV) (u \# ). En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] la memoria de destino.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] el valor que se va a comparar con *dst1*.<br/>                                                                                 |
| <span id="scr1"></span><span id="SCR1"></span>*scr1*<br/>                                                | \[en \] el valor escrito en la memoria de destino si los valores comparados son idénticos.<br/>                               |



 

Esta instrucción realiza una comparación de valores de 32 bits de un solo componente de operando *src0* con *dst1* en 32 bits por dirección de componente *dstAddress*.

Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado. Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.

Si *dst1* es g \# , debe declararse como RAW o Structured.

Si los valores comparados son idénticos, el valor de 32 bits de un solo componente de *SRC1* se escribe en la memoria de destino. De lo contrario, no se cambia la memoria de destino.

El valor original de 32 bits en la memoria de destino siempre se escribe en *dst0*.

Toda la operación se realiza de forma atómica.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.

Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.

Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



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

 

 






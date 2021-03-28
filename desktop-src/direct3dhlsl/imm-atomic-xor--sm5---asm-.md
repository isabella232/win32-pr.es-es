---
title: imm_atomic_xor (SM5-ASM)
description: XOR bit a bit insuficiente a la memoria. Devuelve el valor en memoria antes de la XOR.
ms.assetid: 310037F6-F048-4DE1-9A5C-76C919D9E68B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83503f87ef53474502b1e36ba46cfec1f782f63
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904302"
---
# <a name="imm_atomic_xor-sm5---asm"></a>IMM \_ Atomic \_ XOR (SM5-ASM)

XOR bit a bit insuficiente a la memoria. Devuelve el valor en memoria antes de la XOR.



| IMM \_ Atomic \_ Oex dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\] |
|-------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[en \] contiene el valor de *dst1* antes de XOR.<br/>                                                                  |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[en \] una vista de acceso desordenado (UAV) (u \# ). En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] la dirección de memoria.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | Valor que se va a XOR con *dst1*.<br/>                                                                                          |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un único componente XOR bit a bit de 32 bits de operando *src0* con *dst1* en 32 bits por dirección de componente *dstAddress*.

Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado. Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.

Si *dst1* es g \# , debe declararse como RAW o Structured.

El valor de la memoria *dst1* antes de que se devuelva XOR a *dst0*.

Toda la operación se realiza de forma atómica.

El número de componentes tomado de la dirección viene determinado por la dimensionalidad del recurso declarado en *dst1*.

Si la invocación del sombreador está inactiva, para exammple si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxeles o de ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.

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

 

 






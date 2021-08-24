---
title: imm_atomic_cmp_exch (sm5 - asm)
description: Comparación inmediata e intercambio a memoria.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1014d338687a0798675ed407c0db844c80491833b45628020249bf94b6061b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562420"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a>imm \_ atomic \_ cmp \_ exch (sm5 - asm)

Comparación inmediata e intercambio a memoria.



| imm \_ atomic \_ cmp \_ exch dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swzzle, \] src0 \[ .select component , \_ \] src1 \[ .select \_ component\] |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[out \] Contiene *dst1 antes* de la escritura.<br/>                                                                              |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[en \] Una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La memoria de destino.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] El valor que se comparará con *dst1*.<br/>                                                                                 |
| <span id="scr1"></span><span id="SCR1"></span>*scr1*<br/>                                                | \[en \] El valor escrito en la memoria de destino si los valores comparados son idénticos.<br/>                               |



 

Esta instrucción realiza una comparación de valores de 32 bits de componente único del operando *src0* con *dst1* a 32 bits por dirección *de componente dstAddress*.

Si *dst1* es un u , puede que se haya declarado \# como sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst1* es g \# , debe declararse como sin formato o estructurado.

Si los valores comparados son idénticos, el valor de 32 bits de componente único de *src1* se escribe en la memoria de destino. De lo contrario, no se cambia la memoria de destino.

El valor original de 32 bits de la memoria de destino siempre se escribe en *dst0.*

Toda la operación se realiza de forma atómica.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para derivados, esta instrucción no modifica la memoria *dst1* en absoluto y el valor devuelto es indefinido.

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de los límites, todo el contenido del UAV se vuelve \# \# indefinido.

El direccionamiento fuera de los límites en u o g hace que se devuelva un resultado \# \# indefinido al sombreador en *dst0*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






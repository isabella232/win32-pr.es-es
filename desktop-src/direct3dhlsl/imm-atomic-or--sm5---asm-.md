---
title: imm_atomic_or (sm5 - asm)
description: OR bit a bit inmediato a la memoria. Devuelve el valor en memoria antes de OR.
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4188e8b79cdf4d782ebc926645a4279d08c9682fd0ae254c2ce37c5fbcf46a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982105"
---
# <a name="imm_atomic_or-sm5---asm"></a>imm \_ atomic \_ o (sm5 - asm)

OR bit a bit inmediato a la memoria. Devuelve el valor en memoria antes de OR.



| imm \_ atomic \_ o dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swzzle \] , src0 \[ .select \_ component\] |
|------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[en \] Contiene el valor de *dst1 antes* de OR.<br/>                                                                   |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[en \] una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La dirección de memoria.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | Valor de OR con *dst1.*<br/>                                                                                           |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un único componente de 32 bits OR bit a bit de operando *src0* con *dst1* a 32 bits por dirección de componente *dstAddress*.

Si *dst1* es una u , es posible que se haya declarado como \# sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst1* es g \# , debe declararse como sin formato o estructurado.

Valor de *la memoria dst1* antes de que or se devuelva a *dst0.*

Toda la operación se realiza de forma atómica.

El número de componentes tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *dst1.*

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para los derivados, esta instrucción no modifica la memoria *dst1* en absoluto y el valor devuelto no está definido.

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de límites, todo el contenido del UAV se queda \# \# sin definir.

El direccionamiento fuera de límites en u o g hace que se devuelva un resultado no definido al \# \# sombreador en *dst0.*

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






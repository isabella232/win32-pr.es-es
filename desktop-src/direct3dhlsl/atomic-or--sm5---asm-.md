---
title: atomic_or (sm5 - asm)
description: OR bit a bit atómico en la memoria.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9b86bbdb7d282c14b0e2d30f8e1f996b9c0f4d2f1a09de7b03e549327e309e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794873"
---
# <a name="atomic_or-sm5---asm"></a>atomic \_ o (sm5 - asm)

OR bit a bit atómico en la memoria.



| atomic \_ o dst, dstAddress \[ .swprendle, \] src0 \[ .select \_ (componente)\] |
|--------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[en \] Los componentes de a OR con *src0*. Este valor debe ser una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La dirección de memoria.<br/>                                                                                                                                                |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] Los componentes a OR con *dst*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un único componente or bit a bit de 32 bits de *src0* de operando en *dst* a 32 bits por dirección de componente *dstAddress,* realizado de forma atómica.

El número de componentes tomados de la dirección viene determinado por la dimensionalidad *de dst* u \# o g \# .

Si *dst* es un u \# , se puede declarar como sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst* es g \# , debe declararse como sin formato o estructurado.

No se devuelve nada al sombreador.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para derivados, esta instrucción no modifica la memoria *dst* en absoluto (silenciosamente).

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de límites, todo el contenido del UAV se queda \# \# sin definir.

Fuera de los límites que se direcciona en g (los límites de ese g concreto, en lugar de toda la memoria compartida) hace que todo el contenido de toda la memoria compartida se \# \# vuelva indefinido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






---
title: atomic_imax (sm5 - asm)
description: Entero con signo atómico máximo en memoria.
ms.assetid: E15E9F25-CFC6-435F-B931-A50EA1C8621C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e4cfb806bf6387752255bbd87d0a7095db3cee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360835"
---
# <a name="atomic_imax-sm5---asm"></a>atomic \_ imax (sm5 - asm)

Entero con signo atómico máximo en memoria.



| atomic \_ imax dst, dstAddress \[ .swzzle, \] src0 \[ .select \_ component\] |
|----------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[en \] Los componentes que se comparan con *src0*. Este valor debe ser una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La dirección de memoria.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] Los componentes que se comparan con *dst*.<br/>                                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Esta operación realiza un único componente de 32 bits con signo máximo de *src0* de operando en *dst* a 32 bits por dirección de componente *dstAddress,* realizado de forma atómica.

El número de componentes tomados de la dirección viene determinado por la dimensionalidad *de dst* u \# o g \# .

Si *dst* es un u \# , se puede declarar como sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst* es g \# , debe declararse como sin formato o estructurado.

No se devuelve nada al sombreador.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para derivados, esta instrucción no modifica la memoria *dst* en absoluto (silenciosamente).

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de límites, todo el contenido del UAV se queda \# \# sin definir.

Fuera de los límites que se direcciona en g (los límites de ese g concreto, en lugar de toda la memoria compartida) hace que todo el contenido de toda la memoria compartida se \# \# vuelva indefinido.

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
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






---
title: atomic_cmp_store (SM5-ASM)
description: Comparación atómica y escritura en la memoria.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784978"
---
# <a name="atomic_cmp_store-sm5---asm"></a>\_almacén atómico \_ de CMP (SM5-ASM)

Comparación atómica y escritura en la memoria.



| almacén atómico de \_ CMP \_ , DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_ \] , componente SRC1 \[ . Select. \_\] |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[en \] los componentes que se van a comparar con *src0*. Este valor debe ser una vista de acceso desordenado (UAV) (u \# ). En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] la dirección de memoria.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] el valor de 32 bits para comparar con el *DST*.<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>                                                | \[en \] el valor que se va a escribir en la memoria si los valores comparados son idénticos. <br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una comparación de valores de 32 bits de un solo componente de operando *src0* con *DST* en 32 bits por dirección de componente *dstAddress*.

Si los valores comparados son idénticos, el valor de 32 bits de un solo componente de *SRC1* se escribe en la memoria de destino. De lo contrario, no se cambia el destino.

Toda la operación de comparación y escritura se realiza de forma atómica.

Si el *DST* es una u \# , se puede declarar como sin formato, con tipo o estructurada. Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.

Si *DST* es g \# , debe declararse como RAW o Structured.

El número de componentes tomado de la dirección viene determinado por la dimensionalidad del DST u \# o g \# .

No se devuelve nada al sombreador.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o una instrucción de ejemplo o píxel no modifica la memoria de *DST* en absoluto (en modo silencioso).

Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.

Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida), hace que todo el contenido de toda la memoria compartida quede sin definir.

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

 

 






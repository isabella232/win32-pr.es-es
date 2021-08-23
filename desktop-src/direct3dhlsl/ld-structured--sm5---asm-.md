---
title: ld_structured (sm5 - asm)
description: Lectura de acceso aleatorio de componentes de 1 a 4 de 32 bits desde un búfer estructurado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562315"
---
# <a name="ld_structured-sm5---asm"></a>ld \_ structured (sm5 - asm)

Lectura de acceso aleatorio de componentes de 1 a 4 de 32 bits desde un búfer estructurado.



| : ld \_ structured dst0 \[ .mask \] , srcAddress \[ .select component , \_ \] srcByteOffset \[ .select component , \_ \] src0 \[ .swjunle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] La dirección de los resultados de la operación.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[en \] Especifica el índice de la estructura que se leerá.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[en \] Especifica el desplazamiento de bytes de la estructura desde la que se empieza a leer. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Búfer del que se leerá. Este parámetro debe ser un SRV (t \# ), UAV (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |



 

## <a name="remarks"></a>Comentarios

Los datos leídos de la estructura son equivalentes al pseudocódigo siguiente: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Este pseudocódigo muestra cómo funciona la operación, pero los datos reales no tienen que almacenarse linealmente. Si los datos no se almacenan linealmente, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.

Fuera de los límites que se direccionan en u /t de un componente de 32 bits determinado devuelve 0 para ese componente, excepto si \# \# *srcByteOffset*, más sw swzzle es lo que hace que el acceso fuera de los límites a usted /t , el valor devuelto para todos los componentes \# no está \# definido.

Fuera de los límites que se direccionen en g (los límites de ese g determinado, en lugar de toda la memoria compartida) para cualquier componente de 32 bits determinado devuelve un resultado \# \# indefinido.

*srcByteOffset* es un argumento independiente de *srcAddress* porque normalmente es un literal. Esta separación de parámetros no se ha realizado para atomics en la memoria estructurada.

cs 4 0 y cs 4 1 admiten esta instrucción para \_ \_ \_ \_ UAV, SRV y TGSM.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para los UAV para el entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
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



 

cs \_ 4 \_ 0 y cs 4 1 admiten esta instrucción para \_ \_ UAV, SRV y TGSM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






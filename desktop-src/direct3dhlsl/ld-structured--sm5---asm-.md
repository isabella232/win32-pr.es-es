---
title: ld_structured (SM5-ASM)
description: Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer estructurado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419949"
---
# <a name="ld_structured-sm5---asm"></a>LD \_ estructurado (SM5-ASM)

Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer estructurado.



| : LD \_ estructurado dst0 \[ . Mask \] , srcAddress \[ . Select \_ Component \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] la dirección de los resultados de la operación.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[en \] especifica el índice de la estructura que se va a leer.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[en \] especifica el desplazamiento de bytes de la estructura en la que se va a empezar a leer. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Búfer del que se va a leer. Este parámetro debe ser SRV (t \# ), UAV (u \# ). En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |



 

## <a name="remarks"></a>Observaciones

Los datos leídos de la estructura son equivalentes a los siguientes pseudocódigo: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.

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

En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal. Si los datos no se almacenan de forma lineal, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.

Fuera de los límites que se direccionan en u \# /t \# de cualquier componente de 32 bits dado devuelve 0 para ese componente, excepto si *srcByteOffset*, más swizzle es lo que hace que los límites de los límites tengan acceso a \# la dirección/t \# , el valor devuelto para todos los componentes es indefinido.

Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, devuelve un resultado no definido.

*srcByteOffset* es un argumento independiente de *srcAddress* porque suele ser un literal. Esta separación de parámetros no se ha realizado para Atomics en la memoria estructurada.

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para UAVs para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



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



 

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






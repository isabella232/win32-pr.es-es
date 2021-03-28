---
title: ld_raw (SM5-ASM)
description: Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer sin formato.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983859"
---
# <a name="ld_raw-sm5---asm"></a>LD \_ sin formato (SM5-ASM)

Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer sin formato.



| LD \_ raw dst0 \[ . Mask \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[en \] especifica el desplazamiento del que se va a leer.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] el componente que se va a leer. <br/>                     |



 

## <a name="remarks"></a>Observaciones

*src0* debe ser:

-   Cualquier fase del sombreador: SRV (t \# ) LD St
-   Sombreador de cálculo o sombreador de píxeles: UAV (u \# )
-   Sombreador de cálculo: memoria compartida de grupo de subprocesos (g \# )

*srcByteOffset* especifica el valor de base 32 bits en memoria para una ventana de 4 valores de 32 bits secuenciales en los que se pueden leer los datos, en función de la swizzle y de la máscara de otros parámetros.

Los datos leídos del búfer sin formato son equivalentes a los siguientes pseudocódigo: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Fuera de los límites que se direccionan en u \# /t \# de cualquier componente de 32 bits determinado devuelve 0 para ese componente.

Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, devuelve un resultado no definido.

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

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



 

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






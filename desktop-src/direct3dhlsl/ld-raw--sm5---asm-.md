---
title: ld_raw (sm5 - asm)
description: Lectura de acceso aleatorio de componentes de 1 a 4 de 32 bits desde un búfer sin procesar.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85fd8ec84b574d506a02812b20f4728e3f7a996ec76ad8569645d4c1643b0ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511095"
---
# <a name="ld_raw-sm5---asm"></a>ld \_ raw (sm5 - asm)

Lectura de acceso aleatorio de componentes de 1 a 4 de 32 bits desde un búfer sin procesar.



| ld \_ raw dst0 \[ .mask , \] srcByteOffset \[ .select component , \_ \] src0 \[ .swzzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[en \] Especifica el desplazamiento del que se leerá.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] El componente que se leerá. <br/>                     |



 

## <a name="remarks"></a>Comentarios

*src0* debe ser:

-   Cualquier fase del sombreador: SRV (t \# )ld st
-   Sombreador de cálculo o sombreador de píxeles: UAV (u \# )
-   Sombreador de proceso: memoria compartida del grupo de subprocesos (g \# )

*srcByteOffset* especifica el valor base de 32 bits en memoria para una ventana de 4 valores secuenciales de 32 bits en los que se pueden leer los datos, en función del swzzle y mask de otros parámetros.

Los datos leídos desde el búfer sin formato son equivalentes al pseudocódigo siguiente: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el intervalo del origen y los datos almacenados linealmente.

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

El direccionamiento fuera de límites en u /t de cualquier componente de \# \# 32 bits determinado devuelve 0 para ese componente.

El direccionamiento fuera de límites en g (los límites de ese g determinado, en lugar de toda la memoria compartida) para cualquier componente de 32 bits determinado devuelve un resultado \# \# indefinido.

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para los UAV para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



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



 

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






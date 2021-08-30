---
title: store_raw (sm5 - asm)
description: Escritura de acceso aleatorio de componentes de 1 a 4 de 32 bits en memoria sin tipo.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2452f5b48b410b0a62dbd394c7c0501d99d34ba15c8c78291c02db58d65d090
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118205"
---
# <a name="store_raw-sm5---asm"></a>store \_ raw (sm5 - asm)

Escritura de acceso aleatorio de componentes de 1 a 4 de 32 bits en memoria sin tipo.



| store \_ raw dst0 \[ .write mask , \_ \] dstByteOffset \[ .select component , \_ \] src0 \[ .swzzle\] |
|----------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] La dirección de memoria.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[en \] El desplazamiento.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] Componentes que se escribirán.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza componentes de 1-4 componentes de 32 bits escritos de \* *src0* a *dst0* en el desplazamiento *de dstByteOffset*. No hay ninguna conversión de formato.

*dst0 debe* ser un UAV (u), o en el sombreador de proceso también puede ser memoria compartida del grupo de \# subprocesos (g \# ).

*dstByteOffset* especifica el valor base de 32 bits en memoria para una ventana de 4 valores secuenciales de 32 bits en los que se pueden escribir datos, en función del swzzle y mask de otros parámetros.

La ubicación de los datos escritos es equivalente al pseudocódigo siguiente, que muestra la dirección, el puntero al contenido del búfer y los datos almacenados linealmente.

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(UINT32));
```

Este pseudocódigo muestra cómo funciona la operación, pero los datos reales no tienen que almacenarse linealmente. *dst0* solo puede tener una máscara de escritura que sea una de las siguientes: .x, .xy, .xyz, .xyzw. La máscara de escritura determina el número de componentes de 32 bits que se escribirán sin espacios.

El direccionamiento fuera de límites en u significa que no se escribe nada en la memoria fuera de límites; cualquier parte que esté dentro de los \# límites se escribirá correctamente.

El direccionamiento fuera de límites en g (los límites de ese g determinado, en lugar de toda la memoria compartida) para cualquier componente de 32 bits dado hace que todo el contenido de toda la memoria compartida se vuelva \# \# indefinido.

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción para UAV.

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

 

 






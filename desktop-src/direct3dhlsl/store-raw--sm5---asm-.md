---
title: store_raw (SM5-ASM)
description: Escritura de acceso aleatorio de componentes de 32 bits de 1-4 en memoria sin tipo.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419975"
---
# <a name="store_raw-sm5---asm"></a>almacén \_ sin procesar (SM5-ASM)

Escritura de acceso aleatorio de componentes de 32 bits de 1-4 en memoria sin tipo.



| Almacene la \_ \[ máscara dst0. Write sin formato, el \_ \] \[ componente dstByteOffset. Select \_ \] , src0 \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] la dirección de memoria.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[en \] el desplazamiento.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] los componentes que se van a escribir.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza componentes de 1-4 de componentes de 32 de componente \* escritos desde *src0* en *dst0* en el desplazamiento en *dstByteOffset*. No hay ninguna conversión de formato.

*dst0* debe ser un UAV (u \# ) o, en el sombreador de cálculo, también puede ser la memoria compartida del grupo de subprocesos (g \# ).

*dstByteOffset* especifica el valor de base 32 bits en memoria para una ventana de 4 valores de 32 bits secuenciales en los que se pueden escribir datos, en función de la swizzle y de la máscara de otros parámetros.

La ubicación de los datos escritos es equivalente al siguiente pseudocódigo que muestra la dirección, el puntero al contenido del búfer y los datos almacenados de forma lineal.

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

En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal. *dst0* solo puede tener una máscara de escritura que sea uno de los siguientes:. x,. XY,. XYZ,. xyzw. La máscara de escritura determina el número de componentes de 32 bits que se van a escribir sin huecos.

Fuera del límite, el direccionamiento en u \# significa que no se escribe nada en la memoria fuera de los límites; cualquier parte que esté en los límites se escribe correctamente.

Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, hace que todo el contenido de toda la memoria compartida quede sin definir.

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV.

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

 

 






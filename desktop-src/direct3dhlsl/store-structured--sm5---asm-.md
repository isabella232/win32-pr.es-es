---
title: store_structured (SM5-ASM)
description: Escritura de acceso aleatorio de componentes de 1-4 32 bits en una vista de acceso desordenado de búfer estructurado (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077086"
---
# <a name="store_structured-sm5---asm"></a>almacenamiento \_ estructurado (SM5-ASM)

Escritura de acceso aleatorio de componentes de 1-4 32 bits en una vista de acceso desordenado de búfer estructurado (UAV).



| Almacene la \_ \[ máscara dst0. Write estructurada, el \_ \] \[ componente dstAddress. Select, el componente \_ \] dstByteOffset \[ . Select \_ \] , src0 \[ . swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[en \] la dirección en la que se va a escribir.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[en \] el índice de la estructura que se va a escribir.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] los componentes que se van a escribir.<br/>                     |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza \* los componentes de 32 bits del componente de 1-4 escritos desde *src0* en *dst0* en la dirección de *dstAddress* y *dstByteOffset*. Sin conversión de formato.

*dst0* debe ser UAV (u \# ). En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).

*dstAddress* especifica el índice de la estructura que se va a escribir.

La ubicación de los datos escritos es equivalente a la del pseudocódigo siguiente, que muestra el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
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
                             WriteComponents * sizeof(INT32));
```

En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal. Si los datos no se almacenan de forma lineal, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.

*dst0* solo puede tener una máscara de escritura que sea uno de los siguientes:. x,. XY,. XYZ,. xyzw. La máscara de escritura determina el número de componentes de 32 bits que se van a escribir sin huecos.

Fuera de los límites que se direccionan en u \# casued por *dstAddress* significa que no se escribe nada en la memoria fuera de los límites.

Si el *dstByteOffset*, incluido *dstWriteMask*, es lo que hace que los límites tengan acceso a usted \# , todo el contenido de la UAV se vuelve sin definir.

Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, hace que todo el contenido de toda la memoria compartida quede sin definir.

*dstByteOffset* es un argumento independiente de *dstAddress* porque suele ser un literal. Esta separación de parámetros no se ha realizado para Atomics en la memoria estructurada.

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y TGSM.

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

 

 






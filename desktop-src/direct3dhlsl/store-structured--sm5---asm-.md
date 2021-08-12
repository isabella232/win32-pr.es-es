---
title: store_structured (sm5 - asm)
description: Escritura de acceso aleatorio de componentes de 1 a 4 de 32 bits en una vista de acceso desordenado (UAV) de búfer estructurado.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a220fca330ba4198669245f0336b363c448067613e3f21fce44c9af9325bd9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285760"
---
# <a name="store_structured-sm5---asm"></a>store \_ structured (sm5 - asm)

Escritura de acceso aleatorio de componentes de 1 a 4 de 32 bits en una vista de acceso desordenado (UAV) de búfer estructurado.



| store \_ structured dst0 \[ .write mask , \_ \] dstAddress \[ .select component , \_ \] dstByteOffset \[ .select component , \_ \] src0 \[ .swjunle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descripción                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[en \] La dirección en la que se va a escribir.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[en \] El índice de la estructura que se escribirá.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[en \] Los componentes que se escribirán.<br/>                     |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza componentes de 1 a 4 componentes de 32 bits escritos de \* *src0* a *dst0* en la dirección *de dstAddress* y *dstByteOffset*. Sin conversión de formato.

*dst0* debe ser un UAV (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ).

*dstAddress* especifica el índice de la estructura que se debe escribir.

La ubicación de los datos escritos es equivalente al pseudocódigo siguiente, que muestra el desplazamiento, la dirección, el puntero al contenido del búfer, el intervalo del origen y los datos almacenados linealmente.

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

Este pseudocódigo muestra cómo funciona la operación, pero los datos reales no tienen que almacenarse linealmente. Si los datos no se almacenan linealmente, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.

*dst0* solo puede tener una máscara de escritura que sea una de las siguientes: .x, .xy, .xyz, .xyzw. La máscara de escritura determina el número de componentes de 32 bits que se escribirán sin espacios.

El direccionamiento fuera de límites en u \# casued by *dstAddress* significa que no se escribe nada en la memoria fuera de límites.

Si *dstByteOffset*, incluido *dstWriteMask*, es lo que hace que el acceso fuera de los límites sea , todo el contenido de \# la UAV queda indefinido.

Fuera de los límites que se direcciona en g (los límites de esa g concreta, en lugar de toda la memoria compartida) para cualquier componente de 32 bits dado hace que todo el contenido de toda la memoria compartida se vuelva \# \# indefinido.

*dstByteOffset* es un argumento independiente de *dstAddress* porque normalmente es un literal. Esta separación de parámetros no se ha realizado para atomics en la memoria estructurada.

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción para UAV y TGSM.

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



| Modelo de sombreador                                              | Compatible. |
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

 

 






---
title: resinfo (sm4 - asm)
description: Consulte las dimensiones de un recurso de entrada determinado.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb23a6790c113702e59fc53f85a4d838907fe5ff658c29d83e37e3f620a9dc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095325"
---
# <a name="resinfo-sm4---asm"></a>resinfo (sm4 - asm)

Consulte las dimensiones de un recurso de entrada determinado.



| resinfo \[ \_ uint\|\_rcpFloat \] dest \[ .mask \] , srcMipLevel.select \_ component, srcResource \[ .swincompatibilidadle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[en \] el nivel mip.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en una textura de entrada t o u para la que se consultan \] \# las \# dimensiones. <br/> |



 

## <a name="remarks"></a>Comentarios

*srcMipLevel* se lee como un valor escalar entero sin signo, por lo que se requiere un único selector de componentes para el registro de origen, si no es un valor inmediato escalar.

*dest* recibe \[ width, height, depth o array size, total-mip-count \] , seleccionados por la máscara de escritura.

Los valores de ancho, alto y profundidad devueltos son para el nivel de mip seleccionado por el parámetro *srcMipLevel* y están en número de elementos texel, independientemente del tamaño de los datos de texel. En el caso de los recursos de varios ejemplos (texture2D Array MS), el ancho y el alto también se devuelven en \[ \] los elementos de \# textura, no en los ejemplos.

El recuento total de mip devuelto en *dest.w* no se ven afectados por el *parámetro srcMipLevel.*

En el caso de los UAV \# (u), el número de niveles de mip siempre es 1.

Todos los aspectos de esta instrucción se basan en las características de la vista de recursos enlazada en t \# /u \# , no en el recurso base subyacente.

Los valores devueltos son todos de punto flotante, a menos que se utilice el modificador uint, en cuyo caso los valores \_ devueltos son todos enteros. Si se usa el modificador rcpFloat, todos los valores devueltos son de punto flotante y el ancho, alto y profundidad se devuelven como recíprocos \_ (1,0f/ancho, 1,0f/alto, 1,0f/profundidad), incluido INF si width/height/depth son 0 del comportamiento *srcMipLevel* fuera del intervalo. El modificador rcpFloat solo se aplica a los valores devueltos de ancho, alto y profundidad, y no se aplica a los valores establecidos en 0 y, por tanto, no se devuelven, y tampoco se aplica a las devoluciones de tamaño de \_ matriz.

Swzzle en *srcResource permite* que los valores devueltos se desdoleguen arbitrariamente antes de que se escriban en el destino.

Si *srcResource es* texture1D, el ancho se devuelve en *dest.x* y *dest.yz* se establece en 0.

Si *srcResource* es Texture1DArray, el ancho se devuelve en *dest.x*, el tamaño de la matriz se devuelve *en dest.y* y *dest.z* se establece en 0.

Si *srcResource es* Texture2D, el ancho y el alto se devuelven en *dest.xy* y *dest.z* se establece en 0.

Si *srcResource* es Texture2DArray, el ancho y el alto se devuelven en *dest.xy* y el tamaño de la matriz se *devuelve en dest.z.*

Si *srcResource es* texture3D, el ancho, el alto y la profundidad se devuelven *en dest.xyz*.

Si *srcResource* es textureCube, el ancho y el alto de las dimensiones de cara de cubo individuales se devuelven en *dest.xy* y *dest.z* se establece en 0.

Si *srcResource es* TextureCubeArray, el ancho y el alto de las dimensiones de cara de cubo individuales se devuelven *en dest.xy.* *dest.z* se establece en un valor indefinido.

Si se ha especificado una fijación mip por recurso en *srcResource,* resinfo siempre devuelve el número total de mipmaps en la vista para el recuento de mip, independientemente de la fijación. Sin embargo, si resinfo solicita las dimensiones de un miplevel determinado y el miplevel se ha fijado (por ejemplo, una fijación de 2,2 significa que se han acodado los mips 0 y 1), las dimensiones devueltas no están definidas. Algunas implementaciones devolverán el comportamiento fuera de límites especificado para resinfo cuando el miplevel está fuera del intervalo. Otras implementaciones devolverán las dimensiones del mip como si no se hubieran fijado.

### <a name="restrictions"></a>Restricciones

-   *srcResource* debe ser un registro t \# o u que no sea un \# búfer, pero sea una textura \* .
-   No se permite el direccionamiento relativo de *srcResource.*
-   *srcMipLevel debe* usar un único selector de componentes si no es un valor escalar inmediato.
-   Al capturar de t o u que no tiene nada enlazado, se devuelve 0 para \# \# width, height, depth o arraysize y total-mip-count. En este caso, se sigue respetando el modificador rcpFloat, lo que devuelve INF para \_ los valores devueltos aplicables.
-   Si *srcMipLevel* está fuera del intervalo del número disponible de miplevels en el recurso, el comportamiento de la devolución de tamaño *(dest.xyz*) es idéntico al de un recurso t o u sin \# \# enlazar. El recuento total de mip todavía se devuelve en *dest.w* para este caso.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






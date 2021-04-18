---
title: resinfo (SM4-ASM)
description: Consultar las dimensiones de un recurso de entrada determinado.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419916"
---
# <a name="resinfo-sm4---asm"></a>resinfo (SM4-ASM)

Consultar las dimensiones de un recurso de entrada determinado.



| resinfo \[ \_ uint \|\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Select \_ componente, srcResource \[ . swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[en \] el nivel de MIP.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] una \# \# textura de entrada t o u para la que se consultan las dimensiones. <br/> |



 

## <a name="remarks"></a>Observaciones

*srcMipLevel* se lee como un entero sin signo, por lo que se requiere un selector de componente único para el registro de origen, si no es un valor inmediato escalar.

*dest* recibe \[ el ancho, el alto, la profundidad o el tamaño de la matriz, total-MIP-Count \] , seleccionado por la máscara de escritura.

Los valores de ancho, alto y profundidad devueltos son para el nivel de MIP seleccionado por el parámetro *srcMipLevel* y están en el número de textura, independientemente del tamaño de los datos de textura. En el caso de los recursos multiejemplo (texture2D \[ array \] MS \# ), el ancho y el alto también se devuelven en textura, no ejemplos.

El número total de MIP devuelto en *dest. w* no se ve afectado por el parámetro *srcMipLevel* .

En el caso de UAVs (u \# ), el número de niveles de MIP es siempre 1.

Todos los aspectos de esta instrucción se basan en las características de la vista de recursos enlazadas a la t \# /u \# , no en el recurso base subyacente.

Los valores devueltos son todos los puntos flotantes, a menos que \_ se use el modificador uint, en cuyo caso los valores devueltos son enteros. Si \_ se usa el modificador rcpFloat, todos los valores devueltos son de punto flotante y el ancho, el alto y la profundidad se devuelven como recíprocos (1,0 f/width, 1,0 f/height, 1,0 f/Depth), incluido el archivo INF si width/Height/Depth son 0 del comportamiento de *srcMipLevel* fuera del intervalo. El \_ modificador rcpFloat solo se aplica a los valores de ancho, alto y profundidad devueltos, y no se aplica a los valores establecidos en 0 y, por tanto, no se devuelven, y tampoco se aplica a las devoluciones de tamaño de matriz.

Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.

Si *srcResource* es Texture1D, el ancho se devuelve en *dest. x* y *dest. YZ* se establece en 0.

Si *srcResource* es un Texture1DArray, se devuelve el ancho en *dest. x*, el tamaño de la matriz se devuelve en *dest. y* y *dest. z* se establece en 0.

Si *srcResource* es Texture2D, el ancho y el alto se devuelven en *dest. XY* y *dest. z* se establece en 0.

Si *srcResource* es un Texture2DArray, el ancho y el alto se devuelven en *dest. XY* y el tamaño de la matriz se devuelve en *dest. z*.

Si *srcResource* es Texture3D, el ancho, el alto y la profundidad se devuelven en *dest.XYZ*.

Si *srcResource* es un TextureCube, el ancho y el alto de las dimensiones del cubo individual se devuelven en *dest. XY* y *dest. z* se establece en 0.

Si *srcResource* es TextureCubeArray, el ancho y el alto de las dimensiones de la superficie del cubo individual se devuelven en *dest. XY*. *dest. z* se establece en un valor indefinido.

Si se ha especificado una abrazadera de MIP por recurso en *srcResource*, resinfo siempre devuelve el número total de mapas de bits en la vista para el número de MIP, independientemente de la abrazadera. Sin embargo, si resinfo solicita las dimensiones de un miplevel determinado y se ha fijado el miplevel (por ejemplo, una abrazadera de 2,2 significa que se han fijado MIPS 0 y 1), las dimensiones devueltas no están definidas. Algunas implementaciones devolverán el comportamiento fuera del límite especificado para resinfo cuando el miplevel está fuera del intervalo. Otras implementaciones devolverán las dimensiones de MIP como si no se hubieran fijado.

### <a name="restrictions"></a>Restricciones

-   *srcResource* debe ser un \# registro t o u \# que no sea un búfer, pero es una textura \* .
-   No se permite el direccionamiento relativo de *srcResource* .
-   *srcMipLevel* debe usar un selector de componente único si no es un escalar inmediato.
-   La captura de t \# o u \# que no tiene nada enlazado devuelve 0 para width, height, Depth o tamaño y total-MIP-Count. \_En este caso, se sigue respetando el modificador rcpFloat, con lo que se devuelve inf para los valores devueltos aplicables.
-   Si *srcMipLevel* está fuera del intervalo del número de miplevels disponible en el recurso, el comportamiento de la devolución de tamaño (*dest.XYZ*) es idéntico al de un \# recurso t o u no enlazado \# . El número total de MIP todavía se devuelve en *dest. w* para este caso.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






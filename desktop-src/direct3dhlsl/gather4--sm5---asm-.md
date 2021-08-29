---
title: gather4 (sm5 - asm)
description: Recopila los cuatro elementos de textura que se usarían en una operación de filtrado bi lineal y los empaqueta en un único registro. | gather4 (sm5 - asm)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d613eed2f54db109dbddba59a240b535ccfbc8e4833b874719b6f3d4a51748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067945"
---
# <a name="gather4-sm5---asm"></a>gather4 (sm5 - asm)

Recopila los cuatro elementos de textura que se usarían en una operación de filtrado bi lineal y los empaqueta en un único registro. Esta instrucción solo funciona con texturas 2D o CubeMap, incluidas las matrices. Solo se usan los modos de direccionamiento del muestreador y se usa el nivel superior de cualquier pirámide de mip.



| gather4 \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swzzle \] , srcResource \[ .swlinole \] , srcSampler \[ .select \_ component\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Esta instrucción se comporta como la [**instrucción de**](sample--sm4---asm-.md) ejemplo, pero no se genera una muestra filtrada. Las cuatro muestras que contribuirían al filtrado se colocan en xyzw en orden en sentido contrario a las agujas del reloj, empezando por la muestra en la parte inferior izquierda de la ubicación consultada. Esto es lo mismo que el muestreo de puntos con (u,v) diferencias de coordenadas de textura en las siguientes ubicaciones: (-,+),(+,+),(+,-),(-,-), donde la magnitud de los deltas siempre es la mitad de un texel.

En el caso de las texturas de CubeMap, cuando una superficie bi lineal abarca un borde, se usan los elementos de textura de la cara adyacente. Las esquinas usan las mismas reglas que la [**instrucción de**](sample--sm4---asm-.md) ejemplo; es decir, la esquina desconocida se considera el promedio de las tres esquinas de caras que se están imponiendo.

Hay restricciones de formato de textura que se aplican **a gather4** que se expresan en la lista de formatos.

Swzzle en *srcResource permite* que los valores devueltos se desdoleguen arbitrariamente antes de que se escriban en el destino.

El componente .select en srcSampler elige el componente de la textura de origen \_ (r/g/b/a) del que se leerán 4 elementos de textura. 

Para los formatos con componentes float32, si el valor que se captura está normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar. NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN. Para TextureCubes, se debe producir alguna síntesis del 4.º texel que falta en las esquinas, por lo que no se aplica la devolución de bits sin modificar para el texel sintetizado y se podrían vaciar los desnormados.

En el caso de las implementaciones de hardware, las optimizaciones del filtrado bilineal tradicional que detectan muestras directamente en los elementos de textura y omiten la lectura de los elementos de textura que tendrían el peso 0 no se pueden aprovechar con esta instrucción. *gather4* siempre devuelve todos los elementos de textura solicitados.

Esta instrucción se aplica a las siguientes fases del sombreador:



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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






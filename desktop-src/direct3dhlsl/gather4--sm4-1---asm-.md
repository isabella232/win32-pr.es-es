---
title: gather4 (sm4.1 - asm)
description: Recopila los cuatro elementos de textura que se usarían en una operación de filtrado bi lineal y los empaqueta en un único registro. | gather4 (sm4.1 - asm)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb39918bdb421123cb3e2bfe41931740e271f85a27cf36b8994d493656d91c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457585"
---
# <a name="gather4-sm41---asm"></a>gather4 (sm4.1 - asm)

Recopila los cuatro elementos de textura que se usarían en una operación de filtrado bi lineal y los empaqueta en un único registro.



| gather4 \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swzzle \] , srcResource \[ .swlinole \] srcSampler.r |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Contiene las coordenadas de textura. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de recursos. <br/> El sw swzzle permite que los valores devueltos se desdoleguen arbitrariamente antes de que se escriban *en dest*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler.<br/> Este parámetro debe tener un swzzle .r (rojo), que indica que el valor del canal de R se copia en *dest*. <br/> |



 

## <a name="remarks"></a>Observaciones

Esta operación solo funciona con texturas de canal único 2D o CubeMap. En el caso de las texturas 2D, solo se usan los modos de direccionamiento del muestreador y se usa el nivel superior de cualquier pirámide de mip.

Esta instrucción se comporta como la [instrucción de](sample--sm4---asm-.md) ejemplo, pero no se genera una muestra filtrada. Los cuatro ejemplos que contribuirían al filtrado se colocan en xyzw en orden en sentido contrario a las agujas del reloj, empezando por la muestra en la parte inferior izquierda de la ubicación consultada. Esto es lo mismo que el muestreo de puntos con deltas de coordenadas de textura (u,v) en las siguientes ubicaciones: (-,+),(+,+),(+,-),(-,-), donde la magnitud de los deltas siempre es la mitad de un texel.

En el caso de las texturas de CubeMap cuando una superficie bi lineal abarca un borde, se usan los elementos de textura de la cara adyacente. Las esquinas usan las mismas reglas que la **instrucción de** ejemplo; que es la esquina que no está en la esquina se considera el promedio de las tres esquinas de caras que se están imponiendo.

Las restricciones de formato de textura que se aplican a **las instrucciones de** ejemplo también se aplican a la instrucción **gather4.**

En el caso de las implementaciones de hardware, las optimizaciones del filtrado bilineal tradicional que detectan muestras directamente en los elementos de textura y omiten la lectura de los elementos de textura que tendrían el peso 0 no se pueden aprovechar con **gather4**. **gather4** siempre devuelve todos los elementos de textura solicitados.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






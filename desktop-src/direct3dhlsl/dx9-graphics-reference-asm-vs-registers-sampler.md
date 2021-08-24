---
title: Sampler (Direct3D 9 asm-vs)
description: Un sampler es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo. Hay cuatro muestreadores de sombreador de vértices s0 a s3. Se pueden leer cuatro superficies de textura en un solo paso de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 asm-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bd822dc085243adeb97a4baaedce35b150db311ab6b98c531a3e33731635666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789085"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Sampler (Direct3D 9 asm-vs)

Un sampler es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo. Hay cuatro muestreadores de sombreador de vértices: de0 a s3. Se pueden leer cuatro superficies de textura en un solo paso de sombreador.

Sampler (Asm-vs)s de Direct3D 9 son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada muestreador identifica de forma única una sola superficie de textura, que se establece en el muestreador correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento del dibujo, una textura no se puede establecer simultáneamente como un destino de representación y una textura en una fase.

Dado que hay cuatro muestreadores, se pueden leer hasta cuatro superficies de textura desde en un solo paso de sombreador. Un sampler podría aparecer como el único argumento en la instrucción de carga de textura: [texldl - vs](texldl---vs.md).

En comparación con 3 0, si se usa un sampler, debe declararse al principio del programa de sombreador mediante la instrucción \_ \_ [dcl \_ samplerType (sm3 - vs asm).](dcl-samplertype---vs.md)



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Muestra                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Texturas de vértice en frente \_ a \_ 3 0 (HLSL de DirectX)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 
---
title: Sampler (Direct3D 9 asm-ps)
description: Un sampler es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Sampler, Type (Direct3D 9 asm-ps)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abf8887f229669273b26c9afeb036821842bf19311a752654ba1b5909d943090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982845"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Sampler (Direct3D 9 asm-ps)

Un sampler es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo. Hay registros de fase de muestreo de sombreador de 16 píxeles: s0 a s15. Por lo tanto, se pueden leer hasta 16 superficies de textura en un solo paso de sombreador. Las instrucciones que usan un registro de sampler sonld y texldp.

Sampler debe declararse antes de su uso con la [instrucción dcl \_ samplerType (sm2, sm3 - ps asm).](dcl-samplertype---ps.md)



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Muestra               |      |      |      |      | x    | x     | x    | x    | x     |



 

Los muestreadores son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada muestreador identifica de forma única una sola superficie de textura, que se establece en el muestreador correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento del dibujo, una textura no se puede establecer simultáneamente como un destino de representación y una textura en una fase.

Un sampler puede aparecer como el único argumento en la instrucción de carga de textura: [texldl - ps](texldl---ps.md).

En ps 3 0, si se usa un sampler, debe declararse al principio del programa de sombreador mediante la instrucción \_ \_ [dcl \_ samplerType (sm2, sm3 - ps asm).](dcl-samplertype---ps.md)

El muestreo de una textura con una dimensión superior a la que está presente en las coordenadas de textura no es posible. El muestreo de una textura con una dimensión inferior a la que está presente en las coordenadas de textura omitirá las coordenadas de textura adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
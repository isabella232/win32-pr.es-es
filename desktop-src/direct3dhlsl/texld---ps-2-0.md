---
title: 'texld: ps_2_0 y arriba'
description: Muestrear una textura en un muestreador determinado, usando las coordenadas de textura proporcionadas. Esta instrucción es diferente de la instrucción texld- ps \_ 1 4 usada en la versión \_ 1 4 del sombreador de \_ píxeles.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e718bccc05d871cf3d79ec23530c0c891f484f6980b460d497a878742e1b57c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505814"
---
# <a name="texld---ps_2_0-and-up"></a>texld: ps \_ 2 \_ 0 y up

Muestrear una textura en un muestreador determinado, usando las coordenadas de textura proporcionadas. Esta instrucción es diferente de la [instrucción texld- ps \_ 1 \_ 4](texld---ps-1-4.md) usada en la versión 1 4 del sombreador de \_ píxeles.

## <a name="syntax"></a>Syntax



| texld dst, src0, src1 |
|-----------------------|



 

Donde:

-   dst es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para la muestra de textura.
-   src1 identifica [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s), donde especifica qué número de muestreador de textura se va \# \# a muestrear. El muestreador le ha asociado una textura y un estado de muestreador definidos por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 y ps \_ 2 \_ x

dst debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) y solo se permite la máscara \# .xyzw (máscara predeterminada).

src0 debe ser un registro de [coordenadas](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) de textura (t ) o un registro temporal \# (r ), sin modificador ni [](dx9-graphics-reference-asm-ps-registers-temporary.md) \# swzzle.

src1 debe ser [un sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s ), sin modificador \# ni sw private.

Si el bit de límite D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT no está establecido \_ \_ (en D3DPSHADERCAPS2 0), una instrucción de textura determinada \_ [(texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd)](texldd---ps.md) puede depender, como máximo, del tercer orden. Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:

-   src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst se escribió anteriormente y ahora se vuelve a escribir.

Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un registro temporal [(r](dx9-graphics-reference-asm-ps-registers-temporary.md) ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer \# orden. Una instrucción de textura dependiente<sup>del</sup>orden (n) se deriva de una instrucción de textura (n - 1)<sup>th</sup>-order.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 debe ser [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sin modificador. Swzzle se permite en src0 o src1. El swzzle se aplica a las coordenadas de textura antes de la búsqueda de textura.

## <a name="remarks"></a>Comentarios

Esta instrucción se admite en las siguientes versiones:



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

El número de coordenadas necesarias para que src0 realice la muestra de textura depende de cómo se declaró src1, además del componente .w. Los tipos de sampler se declaran [con dcl \_ samplerType (sm2, sm3 - ps asm).](dcl-samplertype---ps.md) Si src1 se declara como un muestreador 2D, src0 debe contener coordenadas .xy; Si src1 se declara como un sampler de cubo o un sampler de volumen, src0 debe contener coordenadas .xyz. Se permite el muestreo de una textura con menos dimensiones de las que están presentes en la coordenada de textura, ya que se omiten los componentes de coordenadas de textura adicionales.

Si la textura de origen contiene menos de cuatro componentes, los valores predeterminados se colocan en los componentes que faltan. Los valores predeterminados dependen del formato de textura, como se muestra en la tabla siguiente:



| Formato de textura                                                                                          | Valores predeterminados       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ A8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Todos los formatos de profundidad o galería de símbolos                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 

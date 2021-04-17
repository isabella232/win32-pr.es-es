---
title: texld-ps_2_0 y arriba
description: Muestra una textura en una muestra determinada, usando las coordenadas de textura proporcionadas. Esta instrucción es diferente de la instrucción texld-PS \_ 1 \_ 4 utilizada en el sombreador de píxeles versión 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47f47a937123ce252189aac57e922b10c2a015fc
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "106098480"
---
# <a name="texld---ps_2_0-and-up"></a>texld-PS \_ 2 \_ 0 y arriba

Muestra una textura en una muestra determinada, usando las coordenadas de textura proporcionadas. Esta instrucción es diferente de la instrucción [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) utilizada en el sombreador de píxeles versión 1 \_ 4.

## <a name="syntax"></a>Syntax



| texld DST, src0, SRC1 |
|-----------------------|



 

Donde:

-   DST es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.
-   SRC1 identifica la [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , donde \# especifica el número de muestra de textura que se muestra. La muestra le ha asociado una textura y un estado de muestra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 y PS \_ 2 \_ x

DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) y solo se permite la máscara xyzw (máscara predeterminada).

src0 debe ser un registro de [coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sin modificador ni swizzle.

SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador o swizzle.

Si \_ \_ no se establece el bit de límite de D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 \_ 0), una instrucción de textura determinada ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) puede depender, como máximo, de tercer orden. Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:

-   src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   DST se escribió previamente y se ha escrito de nuevo.

Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer orden. Una instrucción de textura dependiente del orden de<sup>TH</sup>se deriva de una instrucción de textura de n-1)<sup>TH</sup>-order.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador. Swizzle se permite en src0 o SRC1. Swizzle se aplica a las coordenadas de textura antes de la búsqueda de textura.

## <a name="remarks"></a>Observaciones

Esta instrucción es compatible con las siguientes versiones:



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      |      | x    | x    | x     | x    | x     |



 

El número de coordenadas necesarias para que src0 realice el ejemplo de textura depende de cómo se declaró SRC1, además del componente. w. Los tipos de muestra se declaran con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Si SRC1 se declara como una muestra 2D, src0 debe contener coordenadas. XY; Si SRC1 se declara como una muestra de cubo o una muestra de volumen, src0 debe contener coordenadas. XYZ. Se permite el muestreo de una textura con menos dimensiones que las presentes en la coordenada de textura, ya que los componentes de coordenadas de textura adicionales se omiten.

Si la textura de origen contiene menos de cuatro componentes, los valores predeterminados se colocan en los componentes que faltan. Los valores predeterminados dependen del formato de textura, tal como se muestra en la tabla siguiente:



| Formato de textura                                                                                          | Valores predeterminados       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ A8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Todos los formatos de profundidad/estarcido                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 

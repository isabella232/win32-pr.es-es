---
title: texldb-PS
description: Instrucción de carga de textura sesgada. Esta instrucción usa el cuarto elemento (. a o. w) para sesgar el nivel de detalle de muestreo de textura justo antes del muestreo.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149345"
---
# <a name="texldb---ps"></a>texldb-PS

Instrucción de carga de textura sesgada. Esta instrucción usa el cuarto elemento (. a o. w) para sesgar el nivel de detalle de muestreo de textura justo antes del muestreo.

## <a name="syntax"></a>Sintaxis



| texldb DST, src0, SRC1 |
|------------------------|



 

Donde:

-   DST es el registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura. Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   SRC1 identifica la [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , donde \# especifica el número de muestra de textura que se muestra. La muestra le ha asociado una textura y un estado de muestra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Para conocer las restricciones que se aplican al usar texldb, vea [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md) Instruction.

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 y PS \_ 2 \_ x

DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) y solo se permite la máscara xyzw (máscara predeterminada).

src0 debe ser un registro de [coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sin modificador ni swizzle.

SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador o swizzle.

Si \_ \_ no se establece el bit Cap de D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 \_ 0), una instrucción de textura determinada (texld, texldp, texldb, texldd) puede depender, como máximo, de tercer orden. Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:

-   src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   DST se escribió previamente y se ha escrito de nuevo.

Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer orden. Una instrucción de textura dependiente del orden de<sup>TH</sup>se deriva de una instrucción de textura de n-1)<sup>TH</sup>-order.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador. Swizzle se permite en SRC1 y, cuando se aplica, los resultados de la búsqueda de texturas son swizzled anteriores antes de escribirse en el DST.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb sesga el nivel de detalle del mipmap, calculado normalmente como parte del proceso de ejemplo por el valor (con signo) de src0. w. Los valores de sesgo positivos darán lugar a que se seleccionen los mipmaps más pequeños y viceversa. En el caso de PS \_ 2 \_ 0 y PS \_ 2 \_ x, los valores de Bias pueden estar en el intervalo \[ de-3,0, + 3,0 \] . En el caso de PS \_ 3 \_ 0, los valores de diferencia pueden estar en el intervalo \[ de-16,0, + 15,0 \] . Los valores de sesgo fuera de estos intervalos producen resultados indefinidos. Se sigue respetando el estado de muestra D3DSAMP \_ MIPMAPLODBIAS y se agrega la inclinación texldb a este, pero en cada píxel. Una vez calculado el nivel de detalle sesgado, se \_ sigue respetando D3DSAMP MAXMIPLEVEL y se muestra la textura. Después de texldb, el contenido de src0 no se ve afectado (a menos que el DST sea el mismo registro).

El número de coordenadas necesarias para que src0 realice el ejemplo de textura depende de cómo se declaró SRC1, además del componente. w. Los tipos de muestra se declaran con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Si SRC1 se declara como una muestra 2D, src0 debe contener coordenadas. xyw; Si SRC1 se declara como una muestra de cubo o una muestra de volumen, src0 debe contener coordenadas. xyzw. Se permite el muestreo de una textura 2D con coordenadas. xyzw (se omite la coordenada. z).

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

 

 
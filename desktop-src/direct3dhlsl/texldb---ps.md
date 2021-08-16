---
title: 'texldb: ps'
description: Instrucción de carga de textura sesgada. Esta instrucción usa el cuarto elemento (.a o .w) para sesgo del nivel de detalle de muestreo de textura justo antes del muestreo.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddf340840e377ee03641ae33c0731f27e90ce4760cad4ddb6c636c1831fa80ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505798"
---
# <a name="texldb---ps"></a>texldb: ps

Instrucción de carga de textura sesgada. Esta instrucción usa el cuarto elemento (.a o .w) para sesgo del nivel de detalle de muestreo de textura justo antes del muestreo.

## <a name="syntax"></a>Syntax



| texldb dst, src0, src1 |
|------------------------|



 

Donde:

-   dst es el registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para la muestra de textura. Consulte [Registro de coordenadas de textura.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s), donde especifica qué número de muestreador de textura se va \# \# a muestrear. El muestreador le ha asociado una textura y un estado de muestreador definidos por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Para ver las restricciones al usar texldb, consulte la instrucción [texld - ps \_ 2 \_ 0 y up.](texld---ps-2-0.md)

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 y ps \_ 2 \_ x

dst debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) y solo se permite la máscara \# .xyzw (máscara predeterminada).

src0 debe ser un registro de [coordenadas](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) de textura (t ) o un registro temporal \# (r ), sin modificador ni [](dx9-graphics-reference-asm-ps-registers-temporary.md) \# swzzle.

src1 debe ser [un sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s ), sin modificador \# ni sw private.

Si no se establece el bit de límite D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 0), una instrucción de textura determinada \_ (texlld, texldp, texldb, texldd) puede depender, como máximo, del tercer orden. Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:

-   src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst se escribió anteriormente y ahora se vuelve a escribir.

Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un registro temporal [(r](dx9-graphics-reference-asm-ps-registers-temporary.md) ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer \# orden. Una instrucción de textura dependiente<sup>del</sup>orden (n) se deriva de una instrucción de textura (n - 1)<sup>th</sup>-order.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

src1 debe ser [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sin modificador. Swzzle se permite en src1 y, cuando se aplica, los resultados de la búsqueda de textura se deslizan previamente antes de escribirse en dst.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb sesgo el nivel de detalle de mipmap, calculado normalmente como parte del proceso de ejemplo por el valor (con firma) en src0.w. Los valores de sesgo positivo darán lugar a la selección de mapas MIP más pequeños y viceversa. Para ps 2 0 y ps 2 x, los valores de sesgo pueden estar dentro del \_ \_ intervalo \_ \_ \[ -3.0, +3.0 \] . Para ps 3 0, los valores de sesgo pueden estar dentro del \_ \_ intervalo \[ -16.0, +15.0 \] . Los valores sesgados fuera de estos intervalos producen resultados no definidos. El estado del muestreador D3DSAMP MIPMAPLODBIAS se sigue respetando, y el sesgo de texldb se agrega a esto, pero por \_ píxel. Una vez calculado el nivel de detalle sesgado, se sigue respetando D3DSAMP MAXMIPLEVEL y se produce la muestra \_ de textura. Después de texldb, el contenido de src0 no se ven afectados (a menos que dst sea el mismo registro).

El número de coordenadas necesarias para que src0 realice la muestra de textura depende de cómo se declaró src1, además del componente .w. Los tipos de sampler se declaran [con dcl \_ samplerType (sm2, sm3 - ps asm).](dcl-samplertype---ps.md) Si src1 se declara como un muestreador 2D, src0 debe contener coordenadas .xyw; si src1 se declara como sampler de cubo o sampler de volumen, src0 debe contener coordenadas .xyzw. Se permite el muestreo de una textura 2D con coordenadas .xyzw (se omite la coordenada .z).

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

 

 
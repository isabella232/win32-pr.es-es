---
title: texldd - ps
description: Muestrea una textura con entradas de degradado adicionales.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966428"
---
# <a name="texldd---ps"></a>texldd - ps

Muestrea una textura con entradas de degradado adicionales.

## <a name="syntax"></a>Sintaxis



| texldd, dst, src0, src1, src2, src3 |
|-------------------------------------|



 

Donde:

-   dst es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para la muestra de textura. Consulte [Registro de coordenadas de textura.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica el registro (s) del muestreador de origen, donde especifica qué número de muestreador de textura se va \# \# a muestrear. El muestreador le ha asociado una textura y un estado de control definidos por la [**enumeración D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).
-   src2 es un registro de origen de entrada que especifica el degradado x.
-   src3 es un registro de origen de entrada que especifica el degradado y.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | X \* | x     | x    | x     |



 

\* Esta instrucción solo es compatible con ps \_ 2 \_ a. No es compatible con ps \_ 2 \_ b. Para obtener más información sobre los perfiles, [**vea D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Esta instrucción muestrea una textura mediante las coordenadas de textura en src0, el muestreador especificado por src1 y los degradados DSX y DSY procedentes de src2 y src3. Los valores de degradado x e y se usan para seleccionar el nivel de mapa mip adecuado de la textura para el muestreo.

Todos los orígenes admiten remolinos arbitrarios.

Todas las máscaras de escritura son válidas en el destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
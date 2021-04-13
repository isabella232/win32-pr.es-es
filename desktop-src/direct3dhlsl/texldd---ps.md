---
title: texldd-PS
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420740"
---
# <a name="texldd---ps"></a>texldd-PS

Muestrea una textura con entradas de degradado adicionales.

## <a name="syntax"></a>Sintaxis



| texldd, DST, src0, SRC1, src2, src3 |
|-------------------------------------|



 

Donde:

-   DST es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura. Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   SRC1 identifica los registros de la muestra de origen \# , donde \# especifica el número de muestra de textura que se muestra. La muestra le ha asociado una textura y un estado de control definido por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).
-   src2 es un registro de origen de entrada que especifica el degradado x.
-   src3 es un registro de origen de entrada que especifica el degradado y.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | x1 \* | x     | x    | x     |



 

\* Esta instrucción solo es compatible con la PS \_ 2 \_ a. No es compatible con PS \_ 2 \_ b. Para obtener más información acerca de los perfiles, consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Esta instrucción muestrea una textura mediante las coordenadas de textura en src0, la muestra especificada por SRC1 y los degradados DSX y DSY provienen de src2 y src3. Los valores de degradado x e y se usan para seleccionar el nivel de mipmap adecuado de la textura para el muestreo.

Todos los orígenes admiten swizzles arbitrarios.

Todas las máscaras de escritura son válidas en el destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
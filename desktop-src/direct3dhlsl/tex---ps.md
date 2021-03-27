---
title: Tex-PS
description: Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura. La textura debe estar enlazada a una fase de textura determinada (n) mediante SetTexture. El muestreo de textura está controlado por SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995410"
---
# <a name="tex---ps"></a>Tex-PS

Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura. La textura debe estar enlazada a una fase de textura determinada (n) mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). El muestreo de textura está controlado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).

## <a name="syntax"></a>Sintaxis



| Tex DST |
|---------|



 

, donde

-   DST es el registro de destino.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| tex                   | x    | x    | x    |      |      |      |       |      |       |



 

El número de registro de destino especifica el número de fase de textura.

El muestreo de textura usa coordenadas de textura para buscar, o muestra, un valor de color en las coordenadas especificadas (u, v, w, q), teniendo en cuenta los atributos de estado de fase de textura.

Los datos de coordenadas de textura se interpolan a partir de los datos de coordenadas de textura de vértices y se asocian a una fase de textura específica. La Asociación predeterminada es una asignación de uno a uno entre el número de fase de textura y el orden de las declaraciones de coordenadas de textura. Esto significa que el primer conjunto de coordenadas de textura definido en el formato de vértice está asociado de forma predeterminada a la fase de textura 0.

Las coordenadas de textura pueden estar asociadas a cualquier fase mediante dos técnicas. Cuando se usa un sombreador de vértices de función fijo o la canalización de funciones fijas, la marca de estado de fase de textura TSS \_ TEXCOORDINDEX se puede usar en [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para asociar coordenadas a una fase. De lo contrario, el sombreador de vértices oTn registra las coordenadas de textura cuando se usa un sombreador de vértices programable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
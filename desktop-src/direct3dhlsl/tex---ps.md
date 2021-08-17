---
title: tex - ps
description: Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura. La textura debe enlazarse a una fase de textura determinada (n) mediante SetTexture. El muestreo de textura se controla mediante SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0646a057fdc2fb96e5f72e7451b9b273191ced22f5092a14fab11a9042c5de25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788114"
---
# <a name="tex---ps"></a>tex - ps

Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura. La textura debe enlazarse a una fase de textura determinada (n) mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). El muestreo de textura se controla [**mediante SetSamplerState.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)

## <a name="syntax"></a>Syntax



| tex dst |
|---------|



 

where

-   dst es el registro de destino.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

El número de registro de destino especifica el número de fase de textura.

El muestreo de textura usa coordenadas de textura para buscar, o muestrear, un valor de color en las coordenadas especificadas (u,v,w,q) teniendo en cuenta los atributos de estado de la fase de textura.

Los datos de coordenadas de textura se interpolan a partir de los datos de coordenadas de textura de vértice y se asocian a una fase de textura específica. La asociación predeterminada es una asignación uno a uno entre el número de fase de textura y el orden de declaración de coordenadas de textura. Esto significa que el primer conjunto de coordenadas de textura definido en el formato de vértice está asociado de forma predeterminada a la fase de textura 0.

Las coordenadas de textura se pueden asociar a cualquier fase mediante dos técnicas. Cuando se usa un sombreador de vértices de función fija o la canalización de función fija, la marca de estado de la fase de textura TSS TEXCOORDINDEX se puede usar \_ [**en SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para asociar coordenadas a una fase. De lo contrario, el sombreador de vértices oTn genera las coordenadas de textura cuando se usa un sombreador de vértices programable.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
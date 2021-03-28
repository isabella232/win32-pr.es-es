---
title: GetSamplePosition (objeto de textura de HLSL de DirectX)
description: Obtiene la posición del ejemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419889"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (objeto de textura de HLSL de DirectX)

Obtiene la posición del ejemplo especificado.



|                                        |
|----------------------------------------|
| RET Object. GetSamplePosition (int s); |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                           | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/> | Un tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.<br/> |
| <span id="s"></span><span id="S"></span>*seg*<br/>                                         | \[en \] el índice de ejemplo basado en cero.<br/>                                                      |



 

## <a name="return-value"></a>Valor devuelto

Devuelve la posición de ejemplo (x, y), un vector de punto flotante de dos componentes.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="remarks"></a>Observaciones

Un sombreador de píxeles se puede evaluar con una frecuencia de muestreo (ejecutar un sombreador de píxeles una vez por ejemplo) o con una frecuencia de píxeles (ejecutar un sombreador de píxeles una vez por píxel). Adjunte la \_ semántica de VP SampleIndex a una entrada de sombreador de píxeles para invocar un sombreador de píxeles a la frecuencia de muestreo; a continuación, el valor de entrada se utiliza como índice de ejemplo al realizar el muestreo del destino de representación.

Puede interpolar una entrada del sombreador de píxeles de varias maneras. Para interpolar en:

-   Un centro de píxeles, no use ninguna semántica.
-   Un ejemplo, use la \_ semántica de SAMPLEINDEX VP.
-   Una ubicación centroide, use el modificador [ \_ centroide](dx-graphics-hlsl-struct.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 






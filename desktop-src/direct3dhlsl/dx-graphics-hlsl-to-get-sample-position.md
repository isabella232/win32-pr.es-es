---
title: GetSamplePosition (objeto de textura HLSL de DirectX)
description: Obtiene la posición del ejemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95be6d9b6c4cbf70aed059399af0892a3c75f0a3462b6ef2b0732e8180f4e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068115"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (objeto de textura HLSL de DirectX)

Obtiene la posición del ejemplo especificado.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                           | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/> | Un tipo de objeto de textura [](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[en \] el índice de ejemplo de base cero.<br/>                                                      |



 

## <a name="return-value"></a>Valor devuelto

Devuelve la posición de muestra (x,y), un vector de punto flotante de dos componentes.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Shader Model 4.1 está disponible en Direct3D 10.1 o posterior.

## <a name="remarks"></a>Comentarios

Un sombreador de píxeles se puede evaluar con frecuencia de ejemplo (ejecutar un sombreador de píxeles una vez por muestra) o con frecuencia de píxeles (ejecutar un sombreador de píxeles una vez por píxel). Adjunte la semántica de SV SampleIndex a una entrada de sombreador de píxeles para invocar un sombreador de píxeles con frecuencia de muestra. A continuación, el valor de entrada se usa como índice de ejemplo al muestrear el destino \_ de representación.

Puede interpolar una entrada de sombreador de píxeles de varias maneras. Para interpolar en:

-   Un centro de píxeles, no use ninguna semántica.
-   Un ejemplo, use la semántica \_ SV SampleIndex.
-   Una ubicación de centroide, use el [ \_ modificador centroide.](dx-graphics-hlsl-struct.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 






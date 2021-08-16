---
title: Función WaveGetLaneCount
description: Devuelve el número de calles de una ola en esta arquitectura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Función HlSL de WaveGetLaneCount
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504743"
---
# <a name="wavegetlanecount-function"></a>Función WaveGetLaneCount

Devuelve el número de calles de una ola en esta arquitectura.

## <a name="syntax"></a>Sintaxis

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El resultado estará entre 4 y 128 e incluye todas las ondas: activas, inactivas o de asistente. El resultado devuelto por esta función puede variar significativamente en función de la implementación del controlador.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 





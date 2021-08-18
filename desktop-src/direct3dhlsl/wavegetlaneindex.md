---
title: Función WaveGetLaneIndex
description: Devuelve el índice del camino actual dentro de la onda actual.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Función HLSL de WaveGetLaneIndex
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb6b0290b46727cdf0d9ce705d2910df003cbc114638a0135be2023bb836202a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721725"
---
# <a name="wavegetlaneindex-function"></a>Función WaveGetLaneIndex

Devuelve el índice del camino actual dentro de la onda actual.

## <a name="syntax"></a>Sintaxis

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Índice de la calle actual. El resultado estará entre 0 y el resultado devuelto por [**WaveGetLaneCount.**](wavegetlanecount.md)

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





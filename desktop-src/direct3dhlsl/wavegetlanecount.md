---
title: WaveGetLaneCount función)
description: Devuelve el número de calles de una onda en esta arquitectura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount de función HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421624"
---
# <a name="wavegetlanecount-function"></a>WaveGetLaneCount función)

Devuelve el número de calles de una onda en esta arquitectura.

## <a name="syntax"></a>Sintaxis

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El resultado estará entre 4 y 128, e incluye todas las ondas: las calles activas, inactivas y/o auxiliares. El resultado devuelto por esta función puede variar significativamente según la implementación del controlador.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





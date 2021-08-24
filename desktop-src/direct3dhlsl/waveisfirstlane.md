---
title: Función WaveIsFirstLane
description: Devuelve true solo para el carril activo de la onda actual con el índice más pequeño.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Función WaveIsFirstLane HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d909d4269db61980325c48b5858d910955512f701fb09adbcb91f5e078fa3b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852715"
---
# <a name="waveisfirstlane-function"></a>Función WaveIsFirstLane

Devuelve true solo para el carril activo de la onda actual con el índice más pequeño.

## <a name="syntax"></a>Sintaxis


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

True solo para el carril activo en la onda actual con el índice más pequeño.

## <a name="remarks"></a>Comentarios

Esta función se puede usar para identificar las operaciones que se van a ejecutar solo una vez por onda.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 





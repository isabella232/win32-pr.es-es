---
title: WaveIsFirstLane función)
description: Devuelve true solo para el carril activo en la ola actual con el índice más pequeño.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane de función HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359521"
---
# <a name="waveisfirstlane-function"></a>WaveIsFirstLane función)

Devuelve true solo para el carril activo en la ola actual con el índice más pequeño.

## <a name="syntax"></a>Sintaxis


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

True solo para el carril activo en la ola actual con el índice más pequeño.

## <a name="remarks"></a>Observaciones

Esta función se puede utilizar para identificar las operaciones que se van a ejecutar solo una vez por cada onda.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





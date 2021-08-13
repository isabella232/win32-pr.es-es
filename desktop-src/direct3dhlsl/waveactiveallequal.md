---
title: Función WaveActiveAllEqual
description: Devuelve true si la expresión es la misma para todos los carriles activos de la ola actual (y, por tanto, uniforme en ella).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Función WaveActiveAllEqual HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786115"
---
# <a name="waveactiveallequal-function"></a>Función WaveActiveAllEqual

Devuelve true si la expresión es la misma para todos los carriles activos de la ola actual (y, por tanto, uniforme en ella).

## <a name="syntax"></a>Sintaxis


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

True si la expresión es la misma para todos los carriles activos de la ola actual.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 





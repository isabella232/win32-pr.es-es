---
title: WaveActiveAllEqual función)
description: Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797248"
---
# <a name="waveactiveallequal-function"></a>WaveActiveAllEqual función)

Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella).

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

True si la expresión es la misma para cada carril activo de la ola actual.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





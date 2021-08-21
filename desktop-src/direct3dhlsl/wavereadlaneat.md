---
title: Función WaveReadLaneAt
description: Devuelve el valor de la expresión para el índice de lane especificado dentro de la ola especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Función HLSL de WaveReadLaneAt
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08fa669f8c4284c26052dd68bdbe9ab4f5b99b80b8bdf9445aa3375f0a87a9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504625"
---
# <a name="wavereadlaneat-function"></a>Función WaveReadLaneAt

Devuelve el valor de la expresión para el índice de lane especificado dentro de la ola especificada.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> <dt>

*laneIndex* 
</dt> <dd>

Índice del carril para el que se devolverá el resultado de *expr.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor resultante es el resultado de *expr*. Será uniforme si *laneIndex* es uniforme.

## <a name="remarks"></a>Comentarios

Esta función es realmente una difusión del valor en *el laneIndex*'th lane.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador.

## <a name="see-also"></a>Vea también

* [Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Shader Model 6](shader-model-6-0.md)

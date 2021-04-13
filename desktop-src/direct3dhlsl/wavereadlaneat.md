---
title: WaveReadLaneAt función)
description: Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt de función HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2020
ms.locfileid: "104420500"
---
# <a name="wavereadlaneat-function"></a>WaveReadLaneAt función)

Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada.

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

Índice de la calle para la que se devolverá el resultado de *expr* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor resultante es el resultado de *expr*. Será uniforme si *laneIndex* es uniforme.

## <a name="remarks"></a>Observaciones

Esta función es realmente una difusión del valor de laneIndex'th Lane.

Esta función se admite desde el modelo de sombreador 6,0, en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





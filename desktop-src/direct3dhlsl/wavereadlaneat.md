---
title: Función WaveReadLaneAt
description: Devuelve el valor de la expresión para el índice de la cadena especificado dentro de la onda especificada.
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
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316487"
---
# <a name="wavereadlaneat-function"></a>Función WaveReadLaneAt

Devuelve el valor de la expresión para el índice de la cadena especificado dentro de la onda especificada.

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

Índice del lane para el que se devolverá el resultado *expr.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor resultante es el resultado de *expr*. Será uniforme si *laneIndex* es uniforme.

## <a name="remarks"></a>Comentarios

Esta función es efectivamente una difusión del valor en *el laneIndex*'th lane.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador.

## <a name="see-also"></a>Consulte también

* [Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Modelo de sombreador 6](shader-model-6-0.md)

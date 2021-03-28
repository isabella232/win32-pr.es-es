---
title: 'ConsumeStructuredBuffer:: consume (función)'
description: Quita un valor del final del búfer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Usar HLSL de función
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076995"
---
# <a name="consume-function"></a>Consume (función)

Quita un valor del final del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

El valor quitado (puede ser una estructura).

## <a name="remarks"></a>Observaciones

T puede ser cualquier tipo de datos, incluida una estructura.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





---
title: ConsumeStructuredBuffer::Consume (Función)
description: Quita un valor del final del búfer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Consumo de la función HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963603"
---
# <a name="consume-function"></a>Consumo de función

Quita un valor del final del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

Valor quitado (puede ser una estructura).

## <a name="remarks"></a>Observaciones

T puede ser cualquier tipo de datos, incluida una estructura.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





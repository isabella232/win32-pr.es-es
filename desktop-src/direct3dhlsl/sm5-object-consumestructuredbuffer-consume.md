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
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486705"
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

## <a name="remarks"></a>Comentarios

T puede ser cualquier tipo de datos, incluida una estructura.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





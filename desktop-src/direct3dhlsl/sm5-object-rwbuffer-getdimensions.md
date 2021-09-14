---
title: FUNCIÓN RWBuffer::GetDimensions
description: Obtiene la longitud del búfer. | FUNCIÓN RWBuffer::GetDimensions
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
keywords:
- Función GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963584"
---
# <a name="rwbuffergetdimensions-function"></a>FUNCIÓN RWBuffer::GetDimensions

Obtiene la longitud del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

Tipo: **uint**

Longitud, en bytes, del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





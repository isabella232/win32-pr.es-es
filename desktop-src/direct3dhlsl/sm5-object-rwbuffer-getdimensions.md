---
title: 'RWBuffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | RWBuffer:: Getdimensions ((función)'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
keywords:
- Getdimensions (de función HLSL
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998209"
---
# <a name="rwbuffergetdimensions-function"></a>RWBuffer:: Getdimensions ((función)

Obtiene la longitud del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*atenuar* \[\]
</dt> <dd>

Tipo: **uint**

La longitud, en bytes, del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





---
title: Función ByteAddressBuffer::Load4(uint, uint)
description: Obtiene cuatro valores y el estado de la operación.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Función Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9e65738acfa8a795dc1431bc3c6bb6242d810227bcdc40abcc8cfdf43dea934
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790383"
---
# <a name="load4uint-uint-function"></a>Función Load4(uint, uint)

Obtiene cuatro valores y el estado de la operación.

## <a name="syntax"></a>Sintaxis

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **uint**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se han tomado valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint4**

Cuatro valores.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[**ByteAddressBuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
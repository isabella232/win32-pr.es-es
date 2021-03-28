---
title: 'ByteAddressBuffer:: Getdimensions ((función)'
description: 'Obtiene la longitud del búfer. | ByteAddressBuffer:: Getdimensions ((función)'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998013"
---
# <a name="byteaddressbuffergetdimensions-function"></a>ByteAddressBuffer:: Getdimensions ((función)

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

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[ByteAddressBuffer](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





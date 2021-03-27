---
title: 'StructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | StructuredBuffer:: Getdimensions ((función)'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362191"
---
# <a name="structuredbuffergetdimensions-function"></a>StructuredBuffer:: Getdimensions ((función)

Obtiene las dimensiones de recursos.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*numStructs* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

El número de estructuras en el recurso.

</dd> <dt>

*STRIDE* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

Intervalo, en bytes, de cada elemento de la estructura.

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

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





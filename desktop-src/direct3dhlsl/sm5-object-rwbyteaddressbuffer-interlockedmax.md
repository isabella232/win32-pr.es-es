---
title: Función RWByteAddressBuffer::InterlockedMax
description: Busca el valor máximo de forma atómica.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Función HLSL de InterlockedMax
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e77f925a0950d3731af58c2c6835867640760371
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963552"
---
# <a name="interlockedmax-function"></a>Función InterlockedMax

Busca el valor máximo de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Dirección de destino.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valor de entrada.

</dd> <dt>

*valor \_ de salida* \[ original\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

El valor original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos con tipo int y uint y variables de memoria compartida. Hay tres usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza un máximo atómico del valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza un máximo atómico del valor en la ubicación del recurso a la que hace referencia dest. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función se reduce a un máximo del valor de dest y value, almacenado en dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

Esta función se admite en los siguientes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
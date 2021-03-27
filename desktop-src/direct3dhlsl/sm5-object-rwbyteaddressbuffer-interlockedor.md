---
title: 'RWByteAddressBuffer:: Interlocked (función)'
description: Realiza una expresión atómica o en el valor.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- HLSL de la función interbloquet
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995277"
---
# <a name="interlockedor-function"></a>Interbloqueo (función)

Realiza una expresión atómica **o** en el valor.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Dirección de destino.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valor de entrada.

</dd> <dt>

*\_ valor original* \[ fuera\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El valor original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida. Hay tres usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza una atomicidad **o** con el valor del registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza una atomicidad **o** con el valor de la ubicación del recurso al que hace referencia *dest*. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función se reduce a **o** con los valores de *dest* y *Value*. El resultado de la operación reemplaza el valor de *dest*. La función sobrecargada tiene una variable de salida adicional, que se establecerá en el valor original de *dest*. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

Esta función se admite en los siguientes tipos de sombreadores:



| VS  | !  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
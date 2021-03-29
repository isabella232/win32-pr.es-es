---
title: 'RWByteAddressBuffer:: InterlockedMin (función)'
description: Busca el valor mínimo, de forma atómica.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin de función HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077774"
---
# <a name="interlockedmin-function"></a>InterlockedMin función)

Busca el valor mínimo, de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedMin(
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

Esta operación solo se puede realizar en los recursos con tipo int y uint y las variables de memoria compartida. Hay tres usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza un mínimo atómico del valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza un mínimo atómico del valor en la ubicación del recurso a la que hace referencia dest. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función reduce a un mínimo el valor de DEST y Value, almacenado en dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

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

 

 
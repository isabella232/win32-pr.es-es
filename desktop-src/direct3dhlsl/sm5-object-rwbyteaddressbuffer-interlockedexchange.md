---
title: FUNCIÓN RWByteAddressBuffer::InterlockedExchange
description: Intercambia un valor de forma atómica.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- Función HLSL de InterlockedExchange
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963555"
---
# <a name="interlockedexchange-function"></a>Función InterlockedExchange

Intercambia un valor de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedExchange(
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

*valor \_ original de* \[ salida\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

El valor original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos escalares y variables de memoria compartida. Hay tres usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación de recursos a la que hace referencia dest. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función se reduce a la operación realizada mediante operaciones locales. Esta operación solo está disponible cuando R es legible y se puede escribir.

Esta función se admite en los siguientes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
|  x  |  x  |  x  |  x  | x   | x   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
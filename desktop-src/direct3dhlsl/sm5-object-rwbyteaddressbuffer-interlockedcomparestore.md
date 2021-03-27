---
title: 'RWByteAddressBuffer:: InterlockedCompareStore (función)'
description: Ccompares la entrada al valor de comparación, de forma atómica.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- InterlockedCompareStore de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904737"
---
# <a name="interlockedcomparestore-function"></a>InterlockedCompareStore función)

Ccompares la entrada al valor de comparación, de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Dirección de destino.

</dd> <dt>

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El valor de comparación.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida. Hay tres usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia dest. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función reduce a la operación realizada mediante operaciones locales.

Esta función se admite en los siguientes tipos de sombreadores:



| VS  | !  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
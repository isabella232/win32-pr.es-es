---
title: 'RWByteAddressBuffer:: InterlockedCompareExchange (función)'
description: Compara la entrada con el valor de comparación e intercambia el resultado, de forma atómica.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- InterlockedCompareExchange de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793006"
---
# <a name="interlockedcompareexchange-function"></a>InterlockedCompareExchange función)

Compara la entrada con el valor de comparación e intercambia el resultado, de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
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

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

El valor de comparación.

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

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Compara de forma atómica el valor de *dest* con *el \_ valor de comparación*, almacena el valor en *dest* si los valores coinciden, devuelve el valor original de *dest* en el *\_ valor original*. Esta operación solo se puede realizar en recursos con tipo **int** o *uint* y variables de memoria compartida. Hay tres usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función reduce a la operación realizada mediante operaciones locales. Esta operación solo está disponible cuando R es legible y grabable.

> [!Note]  
> Si llama a **InterlockedCompareExchange** en un bucle for o [**While**](dx-graphics-hlsl-while.md) del sombreador [**de**](dx-graphics-hlsl-for.md) cálculo, para compilar correctamente, debe usar el atributo **\[ Allow \_ UAV \_ Condition \]** en dicho bucle.

 

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

 

 
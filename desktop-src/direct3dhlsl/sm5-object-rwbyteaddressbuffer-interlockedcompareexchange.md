---
title: FUNCIÓN RWByteAddressBuffer::InterlockedCompareExchange
description: Compara la entrada con el valor de comparación e intercambia el resultado de forma atómica.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Función HLSL interlockedCompareExchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963559"
---
# <a name="interlockedcompareexchange-function"></a>Función InterlockedCompareExchange

Compara la entrada con el valor de comparación e intercambia el resultado de forma atómica.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
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

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valor de comparación.

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

Compara de forma atómica el valor de *dest* para comparar el valor *, \_* almacena el valor en *dest* si los valores coinciden y devuelve el valor original *de dest* en el valor *original. \_* Esta operación solo se puede realizar en recursos con tipo **int** *o uint* y variables de memoria compartida. Hay tres usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación de recursos a la que hace referencia *dest*. Por último, el tercer escenario es cuando R es un tipo de variable local. En este escenario, la función se reduce a la operación realizada mediante operaciones locales. Esta operación solo está disponible cuando R es legible y se puede escribir.

> [!Note]  
> Si llama [**a**](dx-graphics-hlsl-for.md) **InterlockedCompareExchange** [](dx-graphics-hlsl-while.md) en un bucle de sombreador de proceso for o while, para compilar correctamente, debe usar el atributo **\[ allow \_ uav \_ condition \]** en ese bucle.

 

Esta función se admite en los siguientes tipos de sombreadores:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
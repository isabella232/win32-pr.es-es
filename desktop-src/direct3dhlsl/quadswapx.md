---
title: QuadReadAcrossX función)
description: Devuelve el valor local especificado leído de la otra calle de este cuádruple en la dirección X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX de función HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149730"
---
# <a name="quadreadacrossx-function"></a>QuadReadAcrossX función)

Devuelve el valor local especificado leído de la otra calle de este cuádruple en la dirección X.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*localValue* 
</dt> <dd>

El tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor local especificado. Si la calle de origen está inactiva, los resultados son indefinidos.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: QuadReadAcrossY función)
description: Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY de función HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984099"
---
# <a name="quadreadacrossy-function"></a>QuadReadAcrossY función)

Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> QuadReadAcrossY(
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

Valor de origen especificado. Si la calle de origen está inactiva, los resultados son indefinidos.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





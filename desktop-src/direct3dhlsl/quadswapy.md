---
title: Función QuadReadAcrossY
description: Devuelve el valor de origen especificado leído desde el otro lado de este cuadrándido en la dirección Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Función HLSL de QuadReadAcrossY
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f761a3588759e0c27143d16bd8fac5f674f05ae1819a0cdcebc55d6b4bdc6e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672405"
---
# <a name="quadreadacrossy-function"></a>Función QuadReadAcrossY

Devuelve el valor de origen especificado leído desde el otro lado de este cuadrándido en la dirección Y.

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

Tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de origen especificado. Si el camino de origen está inactivo, los resultados son indefinidos.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre los cuatros, consulte [Información general del modelo de sombreador 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Esta función solo se admite desde el modelo de sombreador 6.0 en sombreadores de cálculo y píxeles.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: Función QuadReadAcrossX
description: Devuelve el valor local especificado leído desde el otro lado de este cuadrándido en la dirección X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Función HLSL de QuadReadAcrossX
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672445"
---
# <a name="quadreadacrossx-function"></a>Función QuadReadAcrossX

Devuelve el valor local especificado leído desde el otro lado de este cuadrándido en la dirección X.

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

Tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor local especificado. Si el camino de origen está inactivo, los resultados son indefinidos.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre los cuatros, consulte [Información general del modelo de sombreador 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Esta función solo se admite desde el modelo de sombreador 6.0 en sombreadores de cálculo y píxeles.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





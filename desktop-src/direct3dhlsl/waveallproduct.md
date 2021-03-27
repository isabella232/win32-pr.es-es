---
title: WaveActiveProduct función)
description: Multiplica los valores de la expresión en todas las calles activas de la ola actual y los replica de nuevo en todas las calles activas.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- WaveActiveProduct de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904900"
---
# <a name="waveactiveproduct-function"></a>WaveActiveProduct función)

Multiplica los valores de la expresión en todas las calles activas de la ola actual y los replica de nuevo en todas las calles activas.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor del producto.

## <a name="remarks"></a>Observaciones

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





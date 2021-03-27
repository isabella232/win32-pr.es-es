---
title: WaveActiveBitOr función)
description: Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078603"
---
# <a name="waveactivebitor-function"></a>WaveActiveBitOr función)

Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.

## <a name="syntax"></a>Sintaxis

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor OR bit a bit.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





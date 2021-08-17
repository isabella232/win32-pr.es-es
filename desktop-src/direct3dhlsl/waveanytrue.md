---
title: Función WaveActiveAnyTrue
description: Devuelve true si la expresión es true en cualquiera de los sentidos activos de la ola actual.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Función HLSL de WaveActiveAnyTrue
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721735"
---
# <a name="waveactiveanytrue-function"></a>Función WaveActiveAnyTrue

Devuelve true si la expresión es true en cualquiera de los sentidos activos de la ola actual.

## <a name="syntax"></a>Sintaxis

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

Expresión booleana que se evaluará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

True si la expresión es true en cualquier calle.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 





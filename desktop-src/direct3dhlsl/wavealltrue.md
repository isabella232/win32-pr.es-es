---
title: Función WaveActiveAllTrue
description: Devuelve true si la expresión es true en todos los carriles activos de la ola actual.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- Función WaveActiveAllTrue HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f80c9af3bb9a1be47a3d64f31f0b3c3c610022d3a017a13053c0e4fc7db3a82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504875"
---
# <a name="waveactivealltrue-function"></a>Función WaveActiveAllTrue

Devuelve true si la expresión es true en todos los carriles activos de la ola actual.

## <a name="syntax"></a>Sintaxis

``` syntax
bool WaveActiveAllTrue(
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

True si la expresión es true en todos los carriles.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 





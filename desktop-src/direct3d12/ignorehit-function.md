---
description: Se llama desde cualquier sombreador de llamadas para rechazar el sombreador y finalizar el sombreador.
ms.assetid: ''
title: Función IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474473"
---
# <a name="ignorehit-function"></a>Función IgnoreHit

Se llama desde cualquier [sombreador de llamadas](any-hit-shader.md) para rechazar el sombreador y finalizar el sombreador. La búsqueda de pulsaciones continúa sin confirmar la distancia y los atributos de la posición actual.  La [**llamada a ReportHit**](reporthit-function.md) en el [sombreador de intersección](intersection-shader.md), si hay una, devolverá false.  Se conservan las modificaciones realizadas en la carga del rayo hasta este punto en cualquier sombreador de impacto.

## <a name="syntax"></a>Sintaxis

```
void IgnoreHit();

```


## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)




## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





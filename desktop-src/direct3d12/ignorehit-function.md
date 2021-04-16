---
description: Se llama desde un sombreador de posicionamiento cualquiera para rechazar el acierto y finalizar el sombreador.
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696126"
---
# <a name="ignorehit-function"></a>Función IgnoreHit

Se llama desde un [sombreador de posicionamiento cualquiera](any-hit-shader.md) para rechazar el acierto y finalizar el sombreador. La búsqueda de aciertos continúa sin confirmar la distancia y los atributos para el acierto actual.  La llamada a [**ReportHit**](reporthit-function.md) en el [sombreador de intersección](intersection-shader.md), si hay alguna, devolverá FALSE.  Se conservan las modificaciones realizadas en la carga de Ray hasta este punto en el sombreador de posicionamiento any.

## <a name="syntax"></a>Sintaxis

```
void IgnoreHit();

```


## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)




## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





---
description: Se llama desde cualquier sombreador de llamadas para rechazar el objeto hit y finalizar el sombreador.
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
ms.openlocfilehash: 5626074df107b89473edbe24b9c1cedd25577e7d987746bcf7ec330d2982e27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912799"
---
# <a name="ignorehit-function"></a>Función IgnoreHit

Se llama desde cualquier [sombreador de llamadas](any-hit-shader.md) para rechazar el objeto hit y finalizar el sombreador. La búsqueda de pulsaciones continúa sin confirmar la distancia y los atributos del hit actual.  La [**llamada a ReportHit**](reporthit-function.md) en el [sombreador de](intersection-shader.md)intersección , si hay una, devolverá false.  Se conservan las modificaciones realizadas en la carga del rayo hasta este punto en cualquier sombreador de impacto.

## <a name="syntax"></a>Sintaxis

```
void IgnoreHit();

```


## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)




## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





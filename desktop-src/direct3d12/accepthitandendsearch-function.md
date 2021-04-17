---
description: Se usa en cualquier sombreador de posicionamiento para confirmar el acierto actual y, a continuación, detener la búsqueda de más visitas para el rayo.
ms.assetid: ''
title: Función AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648165"
---
# <a name="accepthitandendsearch-function"></a>Función AcceptHitAndEndSearch

Se usa en [cualquier sombreador de posicionamiento](any-hit-shader.md) para confirmar el acierto actual y, a continuación, detener la búsqueda de más visitas para el rayo. Si hay un sombreador de intersección en ejecución, se detiene la ejecución.  La ejecución pasa al [sombreador de posicionamiento más cercano](closest-hit-shader.md), si está habilitado, con el golpe más cercano registrado hasta el momento.

## <a name="syntax"></a>Sintaxis

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





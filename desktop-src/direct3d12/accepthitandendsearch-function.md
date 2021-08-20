---
description: Se usa en cualquier sombreador de aciertos para confirmar el acierto actual y, a continuación, dejar de buscar más aciertos para el rayo.
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
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813032"
---
# <a name="accepthitandendsearch-function"></a>Función AcceptHitAndEndSearch

Se usa en cualquier [sombreador de](any-hit-shader.md) aciertos para confirmar el acierto actual y, a continuación, dejar de buscar más aciertos para el rayo. Si hay un sombreador de intersección en ejecución, se detiene la ejecución.  La ejecución pasa al [sombreador de impactos](closest-hit-shader.md)más cercano, si está habilitado, con el impacto más cercano registrado hasta ahora.

## <a name="syntax"></a>Sintaxis

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Vea también

* [Referencia de HLSL de rayos de Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)

---
description: Devuelve el valor pasado como parámetro HitKind a ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969824"
---
# <a name="hitkind"></a>HitKind

Devuelve el valor pasado como parámetro **HitKind** a [**ReportHit.**](reporthit-function.md)

## <a name="syntax"></a>Sintaxis

```
uint HitKind();

```



## <a name="remarks"></a>Observaciones

Si la intersección del triángulo de función fija informó de la intersección, **HitKind** será una de HIT **KIND TRIANGLE FRONT \_ \_ \_ \_ FACE** (254) o **HIT KIND TRIANGLE BACK \_ \_ \_ \_ FACE** (255).

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





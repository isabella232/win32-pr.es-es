---
description: Devuelve el valor que se pasa como parámetro HitKind a ReportHit.
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648167"
---
# <a name="hitkind"></a>HitKind

Devuelve el valor que se pasa como parámetro **HitKind** a [**ReportHit**](reporthit-function.md).

## <a name="syntax"></a>Sintaxis

```
uint HitKind();

```



## <a name="remarks"></a>Observaciones

Si la intersección se ha comunicado mediante la intersección de triangular de función fija, **HitKind** será uno de los tipos de golpe de la **\_ \_ \_ \_ cara frontal** (254) o el triángulo de la **\_ especie \_ \_ posterior \_** (255).

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





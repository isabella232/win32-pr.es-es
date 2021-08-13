---
description: Bloqueo para proteger la creación de objetos dentro del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: CBaseRenderer::m_ObjectCreationLock miembro (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429317"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Miembro CBaseRenderer::m \_ ObjectCreationLock

Bloqueo para proteger la creación de objetos dentro del filtro. El filtro mantiene este bloqueo cuando crea el pin de entrada ([**CBaseRenderer::m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o el objeto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md)). Este bloqueo impide que varios subprocesos intenten crear uno de estos objetos al mismo tiempo.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





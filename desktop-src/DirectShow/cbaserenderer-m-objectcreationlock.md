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
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070119"
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

 

 





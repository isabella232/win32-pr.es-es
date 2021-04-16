---
description: Bloqueo para proteger la creación de objetos dentro del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Miembro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671523"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Miembro ObjectCreationLock CBaseRenderer:: m \_

Bloqueo para proteger la creación de objetos dentro del filtro. El filtro contiene este bloqueo cuando crea el PIN de entrada ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o el objeto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)). Este bloqueo impide que varios subprocesos intenten crear uno de estos objetos al mismo tiempo.

## <a name="syntax"></a>Sintaxis


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





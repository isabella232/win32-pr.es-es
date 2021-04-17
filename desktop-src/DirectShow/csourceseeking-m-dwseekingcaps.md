---
description: Funciones de búsqueda.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Miembro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660774"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Miembro dwSeekingCaps CSourceSeeking:: m \_

Funciones de búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Observaciones

De forma predeterminada, el valor se establece en la combinación bit a bit de las marcas siguientes:

-   \_Búsqueda de \_ CanSeekForwards
-   \_Búsqueda de \_ CanSeekBackwards
-   \_Búsqueda de \_ CanSeekAbsolute
-   \_Búsqueda de \_ CanGetStopPos
-   \_Búsqueda de \_ CanGetDuration

Si el filtro admite un conjunto diferente de funcionalidades, Invalide este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





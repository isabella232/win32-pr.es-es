---
description: El método ForceRefresh está obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Método CPosPassThru.ForceRefresh (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915525"
---
# <a name="cpospassthruforcerefresh-method"></a>Método CPosPassThru.ForceRefresh

El `ForceRefresh` método está obsoleto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Originalmente, esta clase se diseñó para almacenar en caché punteros a las interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del pin conectado. El `ForceRefresh` método liberó esas interfaces.

Como se implementa actualmente, esta clase no almacena en caché esas interfaces. Por compatibilidad, el `ForceRefresh` método todavía se incluye, pero devuelve S \_ OK sin hacer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





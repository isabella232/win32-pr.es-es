---
description: El método GetSyncSource recupera el reloj de referencia que usa el filtro. Este método implementa el método IMediaFilter::GetSyncSource.
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Método CBaseFilter.GetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 632350f925f843f05bdf7820bc8c14a4570f152afc741d5ed58f1827ad205251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056555"
---
# <a name="cbasefiltergetsyncsource-method"></a>Método CBaseFilter.GetSyncSource

El `GetSyncSource` método recupera el reloj de referencia que usa el filtro. Este método implementa el [**método IMediaFilter::GetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pclock* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IReferenceClock del**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) reloj.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Comentarios

Si el filtro no usa un reloj de referencia, *\* pClock* se establece en **NULL.** Cuando el método devuelve un resultado, si *\* pClock* no es **NULL,** la **interfaz IReferenceClock** tiene un recuento de referencias pendiente. Asegúrese de liberarlo cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 





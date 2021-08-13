---
description: El método GetSyncSource recupera el reloj de referencia que usa el objeto . Este método implementa el método IMediaFilter::GetSyncSource.
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Método CBaseMediaFilter.GetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658878"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Método CBaseMediaFilter.GetSyncSource

El `GetSyncSource` método recupera el reloj de referencia que usa el objeto . Este método implementa el [**método IMediaFilter::GetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)

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

## <a name="remarks"></a>Observaciones

Si el objeto no usa un reloj de referencia, *\* pClock* se establece en **NULL.** Cuando el método devuelve un resultado, si *\* pClock* no es **NULL,** la **interfaz IReferenceClock** tiene un recuento de referencias pendiente. Asegúrese de liberarla cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





---
description: 'El método GetSyncSource recupera el reloj de referencia que usa el filtro. Este método implementa el método IMediaFilter:: GetSyncSource.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Método CBaseFilter. GetSyncSource (Amfilter. h)
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
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661081"
---
# <a name="cbasefiltergetsyncsource-method"></a>CBaseFilter. GetSyncSource, método

El `GetSyncSource` método recupera el reloj de referencia que usa el filtro. Este método implementa el método [**IMediaFilter:: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClock* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="remarks"></a>Observaciones

Si el filtro no usa un reloj de referencia, *\* pClock* se establece en **null**. Cuando el método devuelve un valor, si *\* pClock* no es **null**, la interfaz **IReferenceClock** tiene un recuento de referencias pendiente. Asegúrese de liberarlo cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





---
description: El método SetSyncSource establece un reloj de referencia para el objeto . Este método implementa el método IMediaFilter::SetSyncSource.
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Método CBaseMediaFilter.SetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273236"
---
# <a name="cbasemediafiltersetsyncsource-method"></a>Método CBaseMediaFilter.SetSyncSource

El `SetSyncSource` método establece un reloj de referencia para el objeto . Este método implementa el [**método IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pclock* 
</dt> <dd>

Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





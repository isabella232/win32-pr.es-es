---
description: El método SetSyncSource notifica a la clase base del reloj de referencia actual.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Método CBaseStreamControl. SetSyncSource (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678892"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>CBaseStreamControl. SetSyncSource, método

El `SetSyncSource` método notifica a la clase base del reloj de referencia actual.

## <a name="syntax"></a>Sintaxis


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRefClock* 
</dt> <dd>

Puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a este método desde dentro del método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro. La clase **CBaseStreamControl** usa la interfaz **IReferenceClock** para asegurarse de que no descarta los ejemplos demasiado rápidamente.

## <a name="examples"></a>Ejemplos


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 





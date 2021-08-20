---
description: El método SetSyncSource notifica a la clase base del reloj de referencia actual.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Método CBaseStreamControl.SetSyncSource (Strmctl.h)
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
ms.openlocfilehash: b2b7fa5a4f627b33bbca1665e3d1ff2c5bc347cfa0e35adec37e0afffa81f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954784"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>Método CBaseStreamControl.SetSyncSource

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

Puntero a la [**interfaz IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Llame a este método desde dentro del [**método IMediaFilter::SetSyncSource del**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) filtro. La **clase CBaseStreamControl** usa la **interfaz IReferenceClock** para asegurarse de que no descarta ejemplos demasiado rápido.

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
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 





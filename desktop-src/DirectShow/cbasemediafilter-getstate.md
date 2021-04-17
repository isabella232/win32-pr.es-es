---
description: 'El método GetState recupera el estado del objeto (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter:: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Método CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670539"
---
# <a name="cbasemediafiltergetstate-method"></a>CBaseMediaFilter. GetState, método

El `GetState` método recupera el estado del objeto (en ejecución, detenido o en pausa). Este método implementa el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Intervalo de tiempo de espera, en milisegundos.

</dd> <dt>

*State* 
</dt> <dd>

Puntero a una variable que recibe un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el estado del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="remarks"></a>Observaciones

En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout* . Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 





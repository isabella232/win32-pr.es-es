---
description: 'El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter:: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661082"
---
# <a name="cbasefiltergetstate-method"></a>CBaseFilter. GetState, método

El `GetState` método recupera el estado del filtro (en ejecución, detenido o en pausa). Este método implementa el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

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

Puntero a una variable que recibe un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el estado del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="remarks"></a>Observaciones

En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout* . Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.

Si el filtro no entrega datos mientras están en pausa, invalide el `GetState` método para que devuelva el valor VFW S no se cumple la \_ \_ \_ indicación cuando el filtro esté en pausa (consulte [entrega de muestras](delivering-samples.md)). Por ejemplo:


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





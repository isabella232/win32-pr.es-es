---
description: El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter::GetState.
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter.GetState (Amfilter.h)
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
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017173"
---
# <a name="cbasefiltergetstate-method"></a>Método CBaseFilter.GetState

El `GetState` método recupera el estado de los filtros (en ejecución, detenido o en pausa). Este método implementa el [**método IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

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

Puntero a una variable que recibe un miembro del tipo enumerado [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) que indica el estado del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Comentarios

En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout.* Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.

Si el filtro no entrega datos mientras está en pausa, invalide el método para devolver el valor VFW S CANT CUE cuando el filtro está en pausa (vea Entrega de `GetState` \_ \_ \_ [ejemplos).](delivering-samples.md) Por ejemplo:


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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 





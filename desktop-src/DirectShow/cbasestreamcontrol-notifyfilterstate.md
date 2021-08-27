---
description: El método NotifyFilterState notifica al pin cuando cambia el estado del filtro.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Método CBaseStreamControl.NotifyFilterState (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131425"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Método CBaseStreamControl.NotifyFilterState

El `NotifyFilterState` método notifica al pin cuando cambia el estado del filtro.

## <a name="syntax"></a>Sintaxis


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nuevo \_ estado* 
</dt> <dd>

Especifica el nuevo estado, como miembro de la [**enumeración FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

</dd> <dt>

*tStart* 
</dt> <dd>

Especifica la hora de inicio. Si el nuevo estado de filtro es State Running, pase el valor \_ del [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) De lo contrario, use el valor predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método hace que [**el método CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) deje de esperar. Llame a este método cada vez que el filtro propietario cambie de estado.

## <a name="examples"></a>Ejemplos


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
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

 

 





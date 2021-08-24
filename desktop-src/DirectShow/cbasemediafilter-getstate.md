---
description: El método GetState recupera el estado del objeto (en ejecución, detenido o en pausa). Este método implementa el método IMediaFilter::GetState.
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Método CBaseMediaFilter.GetState (Amfilter.h)
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
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966705"
---
# <a name="cbasemediafiltergetstate-method"></a>Método CBaseMediaFilter.GetState

El `GetState` método recupera el estado del objeto (en ejecución, detenido o en pausa). Este método implementa el [**método IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

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

Puntero a una variable que recibe un miembro del tipo enumerado [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) que indica el estado del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Comentarios

En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout.* Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





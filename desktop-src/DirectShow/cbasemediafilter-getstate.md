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
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273316"
---
# <a name="cbasemediafiltergetstate-method"></a>Método CBaseMediaFilter.GetState

El método recupera el estado del objeto `GetState` (en ejecución, detenido o en pausa). Este método implementa el [**método IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

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

## <a name="remarks"></a>Observaciones

En la clase base, todas las transiciones de estado son sincrónicas y se omite el parámetro *dwMilliSecsTimeout.* Si una clase derivada realiza transiciones de estado asincrónicas, debe invalidar este método para esperar durante las transiciones de estado, con un tiempo de espera de *dwMilliSecsTimeout* milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





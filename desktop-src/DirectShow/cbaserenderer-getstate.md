---
description: El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Método CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670608"
---
# <a name="cbaserenderergetstate-method"></a>CBaseRenderer. GetState, método

El `GetState` método recupera el estado del filtro (en ejecución, detenido o en pausa).

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

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                            |
| <dl> <dt>**Estado de VFW \_ S \_ \_ intermedio**</dt> </dl> | El filtro está pasando al estado indicado.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Argumento de puntero **nulo** .<br/>                          |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) . Cuando el representador está en pausa, no completa la transición de estado hasta que recibe un ejemplo para representarlo. Si el tiempo de espera expira antes de que se complete la transición de estado, el método devuelve VFW \_ S \_ State \_ Intermediate.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





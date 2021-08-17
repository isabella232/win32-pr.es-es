---
description: El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Método CBaseRenderer.GetState (Renbase.h)
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
ms.openlocfilehash: 532a41bb9e39f844b3a485fc236ae8d03450d45cdcb45d92c8cfa94d9af4a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403414"
---
# <a name="cbaserenderergetstate-method"></a>Método CBaseRenderer.GetState

El `GetState` método recupera el estado de los filtros (en ejecución, detenido o en pausa).

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

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                            |
| <dl> <dt>**VFW \_ S \_ STATE \_ INTERMEDIATE**</dt> </dl> | El filtro está transfiriendo al estado indicado.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | Argumento de puntero **NULL.**<br/>                          |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseFilter::GetState.**](cbasefilter-getstate.md) Cuando el representador está en pausa, no completa la transición de estado hasta que recibe un ejemplo para representarlo. Si el tiempo de espera expira antes de que se complete la transición de estado, el método devuelve VFW \_ S \_ STATE \_ INTERMEDIATE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





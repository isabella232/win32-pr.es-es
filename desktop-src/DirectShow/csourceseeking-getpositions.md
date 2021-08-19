---
description: El método GetPositions recupera la posición actual y la posición de detenerse. Este método implementa el método IMediaSeeking::GetPositions.
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking.GetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073348"
---
# <a name="csourceseekinggetpositions-method"></a>Método CSourceSeeking.GetPositions

El `GetPositions` método recupera la posición actual y la posición de detenerse. Este método implementa el [**método IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que recibe la posición inicial.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que recibe la posición de detenerse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Para el *parámetro pCurrent,* este método devuelve el valor de la variable miembro [**CSourceSeeking::m \_ rtStart,**](csourceseeking-m-rtstart.md) que representa el tiempo de búsqueda más reciente, no la posición de streaming actual. Sin embargo, cuando una aplicación llama a **IMediaSeeking::GetPositions** a través del administrador de gráficos de filtros, los valores normalmente proceden de un filtro de representador, no de un filtro de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





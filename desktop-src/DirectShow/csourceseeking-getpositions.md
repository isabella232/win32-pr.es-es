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
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061708"
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

## <a name="remarks"></a>Observaciones

Para el *parámetro pCurrent,* este método devuelve el valor de la variable miembro [**CSourceSeeking::m \_ rtStart,**](csourceseeking-m-rtstart.md) que representa el tiempo de búsqueda más reciente, no la posición de streaming actual. Sin embargo, cuando una aplicación llama a **IMediaSeeking::GetPositions** a través del administrador de gráficos de filtros, los valores normalmente proceden de un filtro de representador, no de un filtro de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





---
description: 'El método GetPositions recupera la posición actual y la posición de detención. Este método implementa el método IMediaSeeking:: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking. GetPositions (Ctlutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660780"
---
# <a name="csourceseekinggetpositions-method"></a>CSourceSeeking. GetPositions, método

El `GetPositions` método recupera la posición actual y la posición de detención. Este método implementa el método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

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

Puntero a una variable que recibe la posición de detención.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Para el parámetro *pCurrent* , este método devuelve el valor de la variable miembro [**CSourceSeeking:: m \_ rtStart**](csourceseeking-m-rtstart.md) , que representa el tiempo de búsqueda más reciente, no la posición de streaming actual. Sin embargo, cuando una aplicación llama a **IMediaSeeking:: GetPositions** a través del administrador de gráficos de filtro, los valores suelen provienen de un filtro de representador, no de un filtro de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





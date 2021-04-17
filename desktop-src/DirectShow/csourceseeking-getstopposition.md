---
description: 'El método GetStopPosition recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetStopPosition.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Método CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690554"
---
# <a name="csourceseekinggetstopposition-method"></a>CSourceSeeking. GetStopPosition, método

El `GetStopPosition` método recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que recibe la hora de detención, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl> | Valor de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

La hora de detención se especifica mediante la variable miembro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





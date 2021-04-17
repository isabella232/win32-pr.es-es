---
description: 'El método SetMediaTime establece las horas de los medios para este ejemplo. Este método implementa el método IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Método CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670529"
---
# <a name="cmediasamplesetmediatime-method"></a>CMediaSample. SetMediaTime, método

El `SetMediaTime` método establece las horas de los medios para este ejemplo. Este método implementa el método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStart* 
</dt> <dd>

Puntero a la hora de inicio del medio o **null**.

</dd> <dt>

*Pendiente* 
</dt> <dd>

Puntero a la hora de detención del medio o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

La hora de detención del medio debe ser mayor que la hora de inicio del medio. Use **null** para invalidar las horas de los medios.

El parámetro *pendiente* especifica una hora de medio absoluta, pero la variable miembro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) se calcula como un desplazamiento desde *pStart*. En otras palabras, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

Para obtener información sobre las horas de los medios, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 





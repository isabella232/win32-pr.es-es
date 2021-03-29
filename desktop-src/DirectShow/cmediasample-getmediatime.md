---
description: 'El método GetMediaTime recupera las horas de los medios de este ejemplo. Este método implementa el método IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679296"
---
# <a name="cmediasamplegetmediatime-method"></a>CMediaSample. GetMediaTime, método

El `GetMediaTime` método recupera las horas de los medios de este ejemplo. Este método implementa el método [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStart* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio del medio.

</dd> <dt>

*Pendiente* 
</dt> <dd>

Puntero a una variable que recibe la hora de detención del medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                                 |
| <dl> <dt>**\_tiempo medio de VFW E \_ \_ \_ no \_ establecido**</dt> </dl> | No se establecieron tiempos multimedia para este ejemplo.<br/> |



 

## <a name="remarks"></a>Observaciones

La variable miembro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica un desplazamiento desde [**CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), pero el valor recibido por el parámetro *pendiente* es un tiempo medio absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.

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

 

 





---
description: El método SetMediaTime establece los tiempos multimedia de este ejemplo. Este método implementa el método IMediaSample::SetMediaTime.
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Método CMediaSample.SetMediaTime (Amfilter.h)
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
ms.openlocfilehash: 3709a5f487855148b8ad4042f61b74fbe6029ef64e00b751672bf478f1da866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016373"
---
# <a name="cmediasamplesetmediatime-method"></a>Método CMediaSample.SetMediaTime

El `SetMediaTime` método establece los tiempos de medios para este ejemplo. Este método implementa el [**método IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a la hora de inicio del medio o **NULL.**

</dd> <dt>

*Pend* 
</dt> <dd>

Puntero a la hora de detenerse del medio o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

La hora de detenerse del medio debe ser mayor que la hora de inicio del medio. Use **NULL para** invalidar los tiempos de medios.

El *parámetro pEnd* especifica un tiempo multimedia absoluto, pero la variable miembro [**CMediaSample::m \_ MediaEnd**](cmediasample-m-mediaend.md) se calcula como un desplazamiento de *pStart*. En otras palabras, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

Para obtener información sobre las horas de los medios, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 





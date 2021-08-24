---
description: El método GetMediaTime recupera los tiempos multimedia de este ejemplo. Este método implementa el método IMediaSample::GetMediaTime.
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample.GetMediaTime (Amfilter.h)
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
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634685"
---
# <a name="cmediasamplegetmediatime-method"></a>Método CMediaSample.GetMediaTime

El `GetMediaTime` método recupera los tiempos multimedia de este ejemplo. Este método implementa el [**método IMediaSample::GetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio del medio.

</dd> <dt>

*Pend* 
</dt> <dd>

Puntero a una variable que recibe la hora de detenerse del medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                                 |
| <dl> <dt>**TIEMPO DE MEDIOS DE VFW \_ E \_ NO \_ \_ \_ ESTABLECIDO**</dt> </dl> | No se estableció ningún tiempo de medios para este ejemplo.<br/> |



 

## <a name="remarks"></a>Comentarios

La variable miembro [**CMediaSample::m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica un desplazamiento de [**CMediaSample::m \_ MediaStart**](cmediasample-m-mediastart.md), pero el valor recibido por el *parámetro pEnd* es un tiempo multimedia absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.

Para obtener información sobre las horas de medios, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 





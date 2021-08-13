---
description: El método GetTime recupera las horas de secuencia en las que debe comenzar y finalizar este ejemplo. Este método implementa el método IMediaSample::GetTime.
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Método CMediaSample.GetTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 755965864692cf2b34ebaadc6e064a47a7514c69fe891a6a15f1bb364e5345e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655256"
---
# <a name="cmediasamplegettime-method"></a>Método CMediaSample.GetTime

El método recupera las horas de transmisión en las que debe comenzar y finalizar `GetTime` este ejemplo. Este método implementa el [**método IMediaSample::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de secuencia inicial, en unidades de 100 nanosegundos.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de secuencia final, en unidades de 100 nanosegundos. Si el ejemplo no tiene ninguna hora de detenerse, el valor se establece en la hora de inicio más una.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                   | Descripción                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Correcto.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ NO \_ STOP \_ TIME**</dt> </dl>         | El ejemplo tiene una hora de inicio válida, pero no una hora de detenerse.<br/> |
| <dl> <dt>**TIEMPO DE EJEMPLO DE VFW \_ E \_ NO \_ \_ \_ ESTABLECIDO**</dt> </dl> | El ejemplo no tiene marcas de tiempo válidas.<br/>          |



 

## <a name="remarks"></a>Observaciones

Las variables [**miembro CMediaSample::m \_ Start**](cmediasample-m-start.md) y [**CMediaSample::m \_ End**](cmediasample-m-end.md) especifican las marcas de tiempo. La variable [**miembro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica si las marcas de tiempo son válidas.

Para obtener información sobre las marcas de tiempo, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 





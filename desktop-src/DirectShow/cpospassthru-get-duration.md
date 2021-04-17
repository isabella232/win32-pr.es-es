---
description: 'El \_ método get Duration recupera la duración de la secuencia. Este método implementa el método IMediaPosition:: get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Método CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681029"
---
# <a name="cpospassthruget_duration-method"></a>CPosPassThru. Get \_ Duration (método)

El `get_Duration` método recupera la duración de la secuencia. Este método implementa el método [**IMediaPosition:: get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plength* 
</dt> <dd>

Puntero a una variable que recibe la longitud total de la secuencia, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





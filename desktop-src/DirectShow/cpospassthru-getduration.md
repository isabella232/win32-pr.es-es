---
description: 'El método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660126"
---
# <a name="cpospassthrugetduration-method"></a>CPosPassThru. GetDuration, método

El `GetDuration` método recupera la duración de la secuencia. Este método implementa el método [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDuration* 
</dt> <dd>

Puntero a una variable que recibe la duración, en unidades del formato de hora actual.

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

 

 





---
description: 'El método GetAvailable recupera el intervalo de veces que la búsqueda es eficaz. Este método implementa el método IMediaSeeking:: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690513"
---
# <a name="csourceseekinggetavailable-method"></a>CSourceSeeking. GetAvailable, método

El `GetAvailable` método recupera el intervalo de veces que la búsqueda es eficaz. Este método implementa el método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEarliest* 
</dt> <dd>

Puntero a una variable que recibe la hora más temprana para una búsqueda eficaz. La variable se establece en cero.

</dd> <dt>

*Planchas* 
</dt> <dd>

Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz. La variable se establece en el valor de la variable miembro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





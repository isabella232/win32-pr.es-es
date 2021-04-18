---
description: 'El método GetAvailable recupera el intervalo de veces que la búsqueda es eficaz. Este método implementa el método IMediaSeeking:: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Método CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679503"
---
# <a name="cpospassthrugetavailable-method"></a>CPosPassThru. GetAvailable, método

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

Puntero a una variable que recibe la hora más temprana para una búsqueda eficaz.

</dd> <dt>

*Planchas* 
</dt> <dd>

Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz.

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

 

 





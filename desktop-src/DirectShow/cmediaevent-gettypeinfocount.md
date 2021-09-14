---
description: 'Método CMediaEvent.GetTypeInfoCount: recupera el número de interfaces de información de tipos proporcionadas por un objeto .'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Método CMediaEvent.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062471"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Método CMediaEvent.GetTypeInfoCount

Recupera el número de interfaces de información de tipos proporcionadas por un objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pctinfo* 
</dt> <dd>

Puntero al número de interfaces de información de tipos que proporciona el objeto . Si el objeto proporciona información de tipo, este número es 1; De lo contrario, el número es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ POINTER si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaEvent (clase)**](cmediaevent.md)
</dt> </dl>

 

 





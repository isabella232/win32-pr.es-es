---
description: Recupera el número de interfaces de información de tipo proporcionado por un objeto.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Método CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671522"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>CMediaControl. GetTypeInfoCount, método

Recupera el número de interfaces de información de tipo proporcionado por un objeto.

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

Puntero al número de interfaces de información de tipo que proporciona el objeto. Si el objeto proporciona información de tipo, este número es 1; de lo contrario, el número es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero E si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 





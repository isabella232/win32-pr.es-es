---
description: 'Método CMediaControl.GetTypeInfoCount: recupera el número de interfaces de información de tipos proporcionadas por un objeto .'
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Método CMediaControl.GetTypeInfoCount (Ctlutil.h)
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
ms.openlocfilehash: 7b46838278414442d6c6fc64687fe21e02732e83
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095593"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>Método CMediaControl.GetTypeInfoCount

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
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaControl (clase)**](cmediacontrol.md)
</dt> </dl>

 

 





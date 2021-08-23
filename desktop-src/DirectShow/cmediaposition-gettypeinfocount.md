---
description: 'Método CMediaPosition.GetTypeInfoCount: el método GetTypeInfoCount recupera el número de interfaces de información de tipo que proporciona el objeto .'
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Método CMediaPosition.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 032584025d91d6e21b02ed74b26b2e59d55e3a6e044c215d586913d8417a412e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157013"
---
# <a name="cmediapositiongettypeinfocount-method"></a>Método CMediaPosition.GetTypeInfoCount

El `GetTypeInfoCount` método recupera el número de interfaces de información de tipo que proporciona el objeto .

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

Puntero a una variable que recibe el número de interfaces de información de tipos proporcionadas por el objeto . Cuando el método devuelve un resultado, el valor es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Argumento de puntero **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 





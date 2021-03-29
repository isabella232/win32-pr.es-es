---
description: El método GetTypeInfoCount recupera el número de interfaces de información de tipo que proporciona el objeto.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660579"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>CBaseDispatch. GetTypeInfoCount, método

El `GetTypeInfoCount` método recupera el número de interfaces de información de tipo que proporciona el objeto.

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

Puntero a una variable que recibe el número de interfaces de información de tipo proporcionado por el objeto. Cuando el método devuelve, el valor es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                               | Descripción                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 





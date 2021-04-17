---
description: 'El método QueryId recupera el identificador del PIN. Este método implementa el método IPin:: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Método CBasePin. QueryId (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670874"
---
# <a name="cbasepinqueryid-method"></a>CBasePin. QueryId (método)

El `QueryId` método recupera el identificador del PIN. Este método implementa el método [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero al identificador del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                   | Descripción                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>       |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo** .<br/> |



 

## <a name="remarks"></a>Observaciones

Este método devuelve una copia de la variable miembro [**CBasePin:: m \_ pName**](cbasepin-m-pname.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 





---
description: 'El método QueryPinInfo recupera información sobre el código PIN. Este método implementa el método IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670873"
---
# <a name="cbasepinquerypininfo-method"></a>CBasePin. QueryPinInfo, método

El `QueryPinInfo` método recupera información sobre el código PIN. Este método implementa el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntero a una estructura de [**\_ información del PIN**](/windows/win32/api/strmif/ns-strmif-pin_info) que recibe la información del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="remarks"></a>Observaciones

Este método usa la variable miembro [**CBasePin:: m \_ pName**](cbasepin-m-pname.md) para el miembro **achName** de la estructura de información del PIN \_ .

Cuando el método devuelve un valor, si el miembro **pFilter** de la estructura de información del PIN \_ no es **null**, tiene un recuento de referencias pendiente. Cuando haya terminado, asegúrese de liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 





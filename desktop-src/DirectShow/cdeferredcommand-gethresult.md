---
description: El método Gethresult (recupera el valor HRESULT del comando invocado.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Método CDeferredCommand. Gethresult ((Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671769"
---
# <a name="cdeferredcommandgethresult-method"></a>CDeferredCommand. Gethresult (, método

El `GetHResult` método recupera el valor **HRESULT** del comando invocado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phrResult* 
</dt> <dd>

Puntero al valor **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ Abort si **m \_ pQueue** es **null**. De lo contrario, devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IDeferredCommand:: gethresult (**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 





---
description: 'El método ConnectTo recupera un puntero al pin conectado, si existe. Este método implementa el método IPin:: ConnectTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Método CBasePin. ConnectTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670845"
---
# <a name="cbasepinconnectedto-method"></a>CBasePin. ConnectTo (método)

El `ConnectedTo` método recupera un puntero al pin conectado, si existe. Este método implementa el método [**IPin:: ConnectTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppPin* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                           | Descripción                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>             | Argumento de puntero **nulo** .<br/> |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/>      |



 

## <a name="remarks"></a>Observaciones

Si el método se ejecuta correctamente, la interfaz **IPin** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberarlo cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 





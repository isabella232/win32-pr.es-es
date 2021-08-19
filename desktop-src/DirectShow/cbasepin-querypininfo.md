---
description: El método QueryPinInfo recupera información sobre el pin. Este método implementa el método IPin::QueryPinInfo.
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin.QueryPinInfo (Amfilter.h)
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
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823247"
---
# <a name="cbasepinquerypininfo-method"></a>Método CBasePin.QueryPinInfo

El `QueryPinInfo` método recupera información sobre el pin. Este método implementa el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)

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

Puntero a una [**estructura DE INFORMACIÓN \_ de PIN**](/windows/win32/api/strmif/ns-strmif-pin_info) que recibe la información del pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Comentarios

Este método usa la variable [**miembro CBasePin::m \_ pName**](cbasepin-m-pname.md) para el **miembro achName** de la estructura INFO \_ de PIN.

Cuando el método devuelve un resultado, si el **miembro pFilter** de la estructura INFO del PIN no es \_ **NULL,** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 





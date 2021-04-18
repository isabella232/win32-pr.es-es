---
description: El método ReconnectPin interrumpe una conexión de PIN existente y la vuelve a conectar al mismo pin, utilizando un tipo de medio especificado.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Método CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660148"
---
# <a name="cbasefilterreconnectpin-method"></a>CBaseFilter. ReconnectPin, método

El `ReconnectPin` método interrumpe una conexión de PIN existente y lo vuelve a conectar al mismo pin, utilizando un tipo de medio especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.

</dd> <dt>

*p.p.* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio, o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                                               |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | la variable miembro de [**m \_ PGraph**](cbasefilter-m-pgraph.md) es **null**.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtro. Si la interfaz [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) no está disponible, el método llama a [**IFilterGraph:: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 





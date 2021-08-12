---
description: El método ReconnectPin interrumpe una conexión de pin existente y la vuelve a conectar al mismo pin, utilizando un tipo de medio especificado.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Método CBaseFilter.ReconnectPin (Amfilter.h)
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
ms.openlocfilehash: a39cef0ac5a0a7c4f186b8eae90a96a8e26fbf886f819dc7562cb7d8df4e087e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659725"
---
# <a name="cbasefilterreconnectpin-method"></a>Método CBaseFilter.ReconnectPin

El método interrumpe una conexión de pin existente y la vuelve a conectar `ReconnectPin` al mismo pin, utilizando un tipo de medio especificado.

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

Puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | [**La \_ variable miembro m pGraph**](cbasefilter-m-pgraph.md) es **NULL.**<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al [**método IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtros. Si la [**interfaz IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) no está disponible, el método llama a [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 





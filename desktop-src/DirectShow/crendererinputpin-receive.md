---
description: El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método invalida el método CBaseInputPin::Receive.
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Método CRendererInputPin.Receive (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34abaa79431edc76ffc17488e8610e3b8c59b2c626d445d403bf2356d7f6982a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054425"
---
# <a name="crendererinputpinreceive-method"></a>Método CRendererInputPin.Receive

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia. Este método invalida el [**método CBaseInputPin::Receive.**](cbaseinputpin-receive.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método llama al método [**CBaseRenderer::Receive**](cbaserenderer-receive.md) del filtro, que controla la representación. Si se produce un error en ese método, el pin envía un evento \_ EC ERRORABORT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 





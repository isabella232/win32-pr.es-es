---
description: 'El método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método invalida el método CBaseInputPin:: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Método CRendererInputPin. Receive (Renbase. h)
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
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661285"
---
# <a name="crendererinputpinreceive-method"></a>CRendererInputPin. Receive (método)

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia. Este método invalida el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) .

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro, que controla la representación. Si se produce un error en ese método, el PIN envía un \_ evento ERRORABORT de EC.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 





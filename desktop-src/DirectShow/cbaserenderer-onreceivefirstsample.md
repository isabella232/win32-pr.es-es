---
description: Se llama al método OnReceiveFirstSample cuando el filtro recibe una muestra mientras está en pausa.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Método CBaseRenderer.OnReceiveFirstSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157705"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Método CBaseRenderer.OnReceiveFirstSample

Se `OnReceiveFirstSample` llama al método cuando el filtro recibe una muestra mientras está en pausa.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnReceiveFirstSample(
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

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [**método CBaseRenderer::Receive**](cbaserenderer-receive.md) llama a este método. No hace nada en la clase base, pero la clase derivada puede invalidarla. Este método está pensado principalmente para representadores de vídeo. Cuando un representador de vídeo está en pausa, normalmente muestra el primer ejemplo como una imagen fija.

La búsqueda del gráfico mientras está en pausa también hace que se llame a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





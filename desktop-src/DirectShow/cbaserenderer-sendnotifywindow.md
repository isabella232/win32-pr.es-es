---
description: El método SendNotifyWindow notifica al filtro ascendente del identificador de ventana de vídeo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Método CBaseRenderer.SendNotifyWindow (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4956ad2b20040b0d22903d2ffaa2c7b460af9250fe057d106db545173d53a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157502"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Método CBaseRenderer.SendNotifyWindow

El `SendNotifyWindow` método notifica al filtro ascendente del identificador de la ventana de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida del filtro ascendente.

</dd> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana de vídeo o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el pin de salida del filtro ascendente admite la interfaz [**IMediaEventSink,**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) este método le envía el código de evento [**EC NOTIFY \_ \_ WINDOW**](ec-notify-window.md) junto con el identificador de ventana.

Los representadores de vídeo pueden invalidar sus [**métodos CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) para llamar a este método. Proporciona un mecanismo para informar al filtro ascendente del identificador de ventana. Si lo hace, invalide también [**el método CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) y llame `SendNotifyWindow` a con un identificador **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





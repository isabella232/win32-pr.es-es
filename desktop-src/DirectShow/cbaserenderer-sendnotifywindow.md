---
description: El método SendNotifyWindow notifica el filtro de nivel superior del identificador de la ventana de vídeo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Método CBaseRenderer. SendNotifyWindow (Renbase. h)
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
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660384"
---
# <a name="cbaserenderersendnotifywindow-method"></a>CBaseRenderer. SendNotifyWindow, método

El `SendNotifyWindow` método notifica el filtro de nivel superior del identificador de la ventana de vídeo.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de salida del filtro de nivel superior.

</dd> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana de vídeo o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el PIN de salida del filtro de nivel superior admite la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , este método lo envía al código de evento de la [**ventana de \_ notificación \_ de EC**](ec-notify-window.md) junto con el identificador de ventana.

Los representadores de vídeo pueden invalidar sus métodos [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) para llamar a este método. Proporciona un mecanismo para informar del filtro de nivel superior del identificador de ventana. Si lo hace, invalide también el método [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) y llame a `SendNotifyWindow` con un identificador **nulo** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





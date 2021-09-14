---
description: El modo de presentación ha cambiado.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061187"
---
# <a name="ec_display_changed"></a>EC \_ DISPLAY \_ CHANGED

El modo de presentación ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntero a una matriz de interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) para los pines de entrada del representador de vídeo. Si *lParam2* es cero, este parámetro puede ser **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *lParam2* es cero, *lParam1* contiene un solo **puntero IPin** o es igual a **NULL.** Si *lParam2* es mayor que cero, *lParam1* contiene una matriz de punteros **IPin** y *lParam2* da el número de elementos de la matriz.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtro detiene temporalmente el gráfico y, a continuación, desconecta y vuelve a conectar el representador de vídeo. No pasa el evento a la aplicación.

## <a name="remarks"></a>Observaciones

Los representadores de vídeo pueden enviar este evento en respuesta a un [**mensaje \_ DISPLAYCHANGE de WM.**](/windows/desktop/gdi/wm-displaychange) El **mensaje \_ DISPLAYCHANGE de WM** indica que el usuario ha cambiado la resolución de pantalla.

Durante la conexión de anclar, la mayoría de los representadores de vídeo seleccionan un formato basado en el modo de presentación actual. Si cambia el modo de presentación, es posible que el representador de vídeo tenga que elegir otro formato. Al enviar este mensaje, el representador indica al administrador de gráficos de filtros que debe volver a conectarse. Durante la reconexión, el representador puede seleccionar un nuevo formato. Si se produce un error en la reconexión, el administrador de gráficos de filtros envía un [**evento \_ EC ERRORABORT**](ec-errorabort.md) a la aplicación.

### <a name="enhanced-video-renderer"></a>Representador de vídeo mejorado

Un presentador personalizado para [**el representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR) debe enviar este evento al EVR si cambia el dispositivo Direct3D del presentador. Establezca *lParam1* y *lParam2* en cero; EVR omite los parámetros de evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 


---
description: Indica la cantidad de tiempo que un componente está tardando en procesar cada muestra.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb107dd4c895f9819d268e6112c22c0c514e480bf778692f28bc87853aee9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792625"
---
# <a name="ec_processing_latency"></a>LATENCIA \_ DE PROCESAMIENTO DE \_ EC

Indica la cantidad de tiempo que un componente está tardando en procesar cada muestra.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME**) Cantidad de tiempo para procesar cada \* muestra, en unidades de 100 nanosegundos.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Un presentador para el filtro [**Representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR) puede enviar este mensaje a la EVR para notificar al EVR sobre la latencia de procesamiento del presentador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Especifica la distancia de programación de un componente para el procesamiento de muestras.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689952"
---
# <a name="ec_sample_latency"></a>\_latencia de ejemplo de EC \_

Especifica la distancia de programación de un componente para el procesamiento de muestras.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**\_ el tiempo de referencia const** \* ) hasta el punto en que se encuentra el componente, en unidades de 100-nanosegundos. Si este valor es positivo, el componente está detrás de la programación. Si este valor es negativo, el componente está por encima de la programación.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Un presentador personalizado para el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) puede enviar este mensaje a EVR para notificar a evr si el presentador está por detrás de la programación o por encima de la programación.

La manera más sencilla de calcular *lParam1* es: *QPC Now*   *QPC Target*, donde *QPC Now* es ahora la hora de reloj y *QPC Target* es el tiempo de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 


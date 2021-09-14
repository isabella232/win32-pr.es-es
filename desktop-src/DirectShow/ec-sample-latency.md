---
description: Especifica el retraso en la programación de un componente para el procesamiento de muestras.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161513"
---
# <a name="ec_sample_latency"></a>LATENCIA \_ DE EJEMPLO DE \_ EC

Especifica el retraso en la programación de un componente para el procesamiento de muestras.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME** \* ) Lo lejos que está el componente, en unidades de 100 nanosegundos. Si este valor es positivo, el componente está detrás de la programación. Si este valor es negativo, el componente se adelanta a la programación.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Un presentador personalizado para el filtro [**Representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR) puede enviar este mensaje al EVR para notificar al EVR si el presentador está detrás de la programación o antes de la programación.

La manera más sencilla de calcular *lParam1* es: *QPC now*   *QPC target*, donde *QPC* ahora es la hora del reloj y el destino *de QPC* es el tiempo de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 


---
description: Especifica el retraso en la programación de un componente para el procesamiento de muestras.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686155"
---
# <a name="ec_sample_latency"></a>LATENCIA \_ DE EJEMPLO DE \_ EC

Especifica el retraso en la programación de un componente para el procesamiento de muestras.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME**) Lo \* lejos que está el componente, en unidades de 100 nanosegundos. Si este valor es positivo, el componente está detrás de la programación. Si este valor es negativo, el componente está por delante de la programación.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Un presentador personalizado para el filtro [**Representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR) puede enviar este mensaje al EVR para notificar al EVR si el presentador está detrás de la programación o antes de la programación.

La manera más sencilla de calcular *lParam1* es: *QPC ahora* destino *QPC*, donde *QPC* ahora es la hora del reloj y el destino *de QPC* es el tiempo de presentación.   

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 


---
description: Un filtro solicita que se reinicie el gráfico.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161539"
---
# <a name="ec_need_restart"></a>EC \_ NEED \_ RESTART

Un filtro solicita que se reinicie el gráfico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtro pausa y reinicia el gráfico. No pasa el evento a la aplicación.

## <a name="remarks"></a>Observaciones

Si un filtro rechaza una muestra en medio de una secuencia, el pin ascendente dejará de entregar muestras. El filtro puede reiniciar la secuencia mediante el envío de este evento. Por ejemplo, el representador de audio podría perder el acceso al dispositivo de sonido, porque una ventana de vídeo ha perdido el foco. En ese momento, el representador de audio comienza a rechazar ejemplos. Cuando recupera el acceso al dispositivo de sonido, envía este evento para reiniciar la secuencia de audio.

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

 

 





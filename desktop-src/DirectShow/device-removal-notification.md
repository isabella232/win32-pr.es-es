---
description: Notificación de eliminación de dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificación de eliminación de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103998039"
---
# <a name="device-removal-notification"></a>Notificación de eliminación de dispositivo

Si el usuario quita un Plug and Play dispositivo que estaba usando el gráfico, el administrador de gráficos de filtros envía un evento de [**\_ \_ pérdida de dispositivo EC**](ec-device-lost.md) . Si el dispositivo vuelve a estar disponible, el administrador de gráficos de filtros expone otro evento de **dispositivo de EC \_ \_ perdido** . Sin embargo, el estado anterior del filtro de captura ya no es válido. La aplicación debe volver a generar el gráfico para usar el dispositivo.

DirectShow no envía ningún evento cuando se conecta un nuevo dispositivo. Para saber cuándo está disponible un nuevo dispositivo, la aplicación puede supervisar los mensajes de la ventana de WM \_ DEVICECHANGE. Para obtener más información, vea "administración de dispositivos" en la documentación de Platform SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




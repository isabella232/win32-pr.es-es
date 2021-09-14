---
description: Notificación de eliminación de dispositivos
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notificación de eliminación de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062360"
---
# <a name="device-removal-notification"></a>Notificación de eliminación de dispositivos

Si el usuario quita un dispositivo Plug and Play que usaba el grafo, el administrador de gráficos de filtro publica un evento [**\_ EC DEVICE \_ LOST.**](ec-device-lost.md) Si el dispositivo vuelve a estar disponible, el administrador de gráficos de filtros publica otro **evento EC \_ DEVICE \_ LOST.** Sin embargo, el estado anterior del filtro de captura ya no es válido. La aplicación debe recompilar el gráfico para usar el dispositivo.

DirectShow no envía ningún evento cuando un nuevo dispositivo está conectado. Para obtener información sobre cuándo está disponible un nuevo dispositivo, la aplicación puede supervisar los mensajes de la ventana WM \_ DEVICECHANGE. Para más información, consulte "Administración de dispositivos" en la documentación de Platform SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




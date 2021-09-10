---
title: Proporcionar actualizaciones de estado
description: Proporcionar actualizaciones de estado
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Macro MCIWndSetActiveTimer
- Macro MCIWndSetInactiveTimer
- Macro MCIWndGetActiveTimer
- Macro MCIWndGetInactiveTimer
- Macro MCIWndSetTimers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372175"
---
# <a name="providing-status-updates"></a>Proporcionar actualizaciones de estado

MCIWnd usa temporizadores para actualizar periódicamente la información de la barra de título y la barra de desplazamiento de la ventana, y para enviar mensajes de notificación a la ventana primaria. Un temporizador controla el período de actualización de la ventana activa de MCIWnd y un segundo temporizador controla el período de actualización para las ventanas MCIWnd que están inactivas. La aplicación puede usar las macros de temporizador MCIWnd para recuperar la configuración actual del temporizador y ajustar los períodos de actualización.

Puede establecer el período de actualización utilizado por el temporizador de ventana activo mediante la macro [**MCIWndSetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) Esta macro establece el período usado por MCIWnd para actualizar la barra de seguimiento, actualizar la posición de reproducción notificada en la barra de título de la ventana y notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual utilizado por el temporizador de ventana activo mediante la macro [**MCIWndGetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) El período de actualización predeterminado para el temporizador de ventana activo es de 500 milisegundos.

Puede establecer el período de actualización utilizado por el temporizador de ventana inactivo mediante la macro [**MCIWndSet NoTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) Esta macro establece el período usado por MCIWnd para actualizar la barra de seguimiento, actualizar la posición de reproducción notificada en el título de la ventana y notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual utilizado por el temporizador de ventana inactivo mediante la macro [**MCIWndGetInactiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) El período de actualización predeterminado para el temporizador de ventana inactiva es de 2000 milisegundos.

La aplicación puede establecer simultáneamente el período de actualización para ambos temporizadores mediante la macro [**MCIWndSetTimers.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) El almacenamiento para el valor del período de actualización está limitado a 16 bits. Si se necesita una cantidad mayor para cualquier período de actualización, establezca los temporizadores individualmente.

 

 





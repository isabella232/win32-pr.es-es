---
title: Proporcionar actualizaciones de estado
description: Proporcionar actualizaciones de estado
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Macro MCIWndSetActiveTimer
- Macro MCIWndSetCiónTimer
- Macro MCIWndGetActiveTimer
- Macro MCIWndGetCiónTimer
- Macro MCIWndSetTimers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71ad60ce3970c21adec75af04f3c896eef4c933816002bc8b4c8c3acabcd5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037585"
---
# <a name="providing-status-updates"></a>Proporcionar actualizaciones de estado

MCIWnd usa temporizadores para actualizar periódicamente la información en la barra de título y la barra de desplazamiento de la ventana, y para enviar mensajes de notificación a la ventana primaria. Un temporizador controla el período de actualización de la ventana activa de MCIWnd y un segundo temporizador controla el período de actualización para las ventanas MCIWnd que están inactivas. La aplicación puede usar las macros de temporizador MCIWnd para recuperar la configuración actual del temporizador y ajustar los períodos de actualización.

Puede establecer el período de actualización utilizado por el temporizador de ventana activa mediante la macro [**MCIWndSetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) Esta macro establece el período utilizado por MCIWnd para actualizar la barra de seguimiento, actualizar la posición de reproducción notificada en la barra de título de la ventana y notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual utilizado por el temporizador de ventana activo mediante la macro [**MCIWndGetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) El período de actualización predeterminado para el temporizador de ventana activa es de 500 milisegundos.

Puede establecer el período de actualización utilizado por el temporizador de ventana inactiva mediante la macro [**MCIWndSetFracciónTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) Esta macro establece el período utilizado por MCIWnd para actualizar la barra de seguimiento, actualizar la posición de reproducción notificada en el título de la ventana y notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual utilizado por el temporizador de ventana inactiva mediante la macro [**MCIWndGetCiónTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) El período de actualización predeterminado para el temporizador de ventana inactiva es de 2000 milisegundos.

La aplicación puede establecer simultáneamente el período de actualización de ambos temporizadores mediante la macro [**MCIWndSetTimers.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) El almacenamiento para el valor del período de actualización está limitado a 16 bits. Si se necesita una cantidad mayor para cualquier período de actualización, establezca los temporizadores individualmente.

 

 





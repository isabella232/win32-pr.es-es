---
title: Proporcionar actualizaciones de estado
description: Proporcionar actualizaciones de estado
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer (macro)
- MCIWndSetInactiveTimer (macro)
- MCIWndGetActiveTimer (macro)
- MCIWndGetInactiveTimer (macro)
- MCIWndSetTimers (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418623"
---
# <a name="providing-status-updates"></a>Proporcionar actualizaciones de estado

MCIWnd usa temporizadores para actualizar periódicamente la información en la barra de título y la barra de desplazamiento de la ventana, y para enviar mensajes de notificación a la ventana primaria. Un temporizador controla el período de actualización de la ventana de MCIWnd activa y un segundo temporizador controla el período de actualización de las ventanas MCIWnd que están inactivas. La aplicación puede usar las macros de temporizador de MCIWnd para recuperar la configuración actual del temporizador y ajustar los períodos de actualización.

Puede establecer el período de actualización utilizado por el temporizador de la ventana activa mediante la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) . Esta macro establece el período utilizado por MCIWnd para actualizar el control TrackBar, para actualizar la posición de reproducción notificada en la barra de título de la ventana y para notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual usado por el temporizador de la ventana activa mediante la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) . El período de actualización predeterminado para el temporizador de la ventana activa es de 500 milisegundos.

Puede establecer el período de actualización utilizado por el temporizador de la ventana inactiva mediante la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) . Esta macro establece el período utilizado por MCIWnd para actualizar la barra de control, para actualizar la posición de reproducción notificada en el título de la ventana y para notificar a la ventana primaria que el medio ha cambiado. Puede recuperar el período de actualización actual usado por el temporizador de la ventana inactiva mediante la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) . El período de actualización predeterminado para el temporizador de la ventana inactiva es de 2000 milisegundos.

La aplicación puede establecer simultáneamente el período de actualización de ambos temporizadores mediante la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) . El almacenamiento para el valor del período de actualización está limitado a 16 bits. Si se necesita una cantidad mayor para cada período de actualización, establezca los temporizadores individualmente.

 

 





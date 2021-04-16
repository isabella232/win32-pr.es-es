---
title: Mensajes en Active Directory Domain Services
description: Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4,0 con Service Pack 6a (SP6a) y posterior con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory mensajes de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656221"
---
# <a name="messages-in-active-directory-domain-services"></a>Mensajes en Active Directory Domain Services

Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4,0 con Service Pack 6a (SP6a) y posterior con DSClient. También son funcionales en estaciones de trabajo de Windows 98/95 con IE 4.01 y versiones posteriores y DSClient. Sin embargo, si las páginas de propiedades de selección MultiSelect se inician desde el Shell, el mensaje de [**\_ \_ \_ error de notificaciones de WM ADSPROP**](wm-adsprop-notify-error.md) y sus funciones auxiliares correspondientes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) y [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) , no estarán funcionales y no se mostrarán. Si las páginas de propiedades de selección MultiSelect se inician en una herramienta de administración, por ejemplo, usuarios y equipos de AD, todos los mensajes estarán funcionales y estarán disponibles para que se muestren en las páginas de propiedades de selección MultiSelect.

Active Directory Domain Services usar los siguientes mensajes:

-   [**\_solicitud de ADSPROP de WM \_ \_**](wm-adsprop-notify-apply.md)
-   [**\_ \_ notificar cambio de ADSPROP de WM \_**](wm-adsprop-notify-change.md)
-   [**\_error de \_ notificación de ADSPROP de WM \_**](wm-adsprop-notify-error.md)
-   [**\_salida de \_ notificación de ADSPROP de WM \_**](wm-adsprop-notify-exit.md)
-   [**\_ \_ notificar a \_ primer plano ADSPROP de WM**](wm-adsprop-notify-foreground.md)
-   [**\_ADSPROP \_ notificar a \_ PAGEHWND de WM**](wm-adsprop-notify-pagehwnd.md)
-   [**\_ADSPROP \_ notificar a \_ PAGEINIT de WM**](wm-adsprop-notify-pageinit.md)
-   [**\_ADSPROP \_ notificar \_ SETFOCUS de WM**](wm-adsprop-notify-setfocus.md)
-   [**hoja de ADSPROP de WM \_ \_ \_ creación**](wm-adsprop-sheet-create.md)
-   [**\_notificación de \_ cierre de hoja DSA \_ de WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ crear notificación de la hoja DSA de WM \_**](wm-dsa-sheet-create-notify.md)

 

 





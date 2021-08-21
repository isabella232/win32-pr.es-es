---
title: Mensajes en Active Directory Domain Services
description: Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4.0 con Service Pack 6a (SP6a) y versiones posteriores con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory Messages AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025923"
---
# <a name="messages-in-active-directory-domain-services"></a>Mensajes en Active Directory Domain Services

Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4.0 con Service Pack 6a (SP6a) y versiones posteriores con DSClient. También son funcionales en Windows de trabajo 98/95 con IE4.01 y versiones posteriores y DSClient. Sin embargo, si se inician páginas de propiedades de selección múltiple desde el shell, el mensaje DE [**\_ ERROR WM ADSPROP NOTIFY \_ \_ y**](wm-adsprop-notify-error.md) sus funciones auxiliares [**correspondientes, ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) y [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) no son funcionales y no se mostrarán. Si las páginas de propiedades de selección múltiple se inician dentro de una herramienta de administración, por ejemplo, Usuarios y equipos de AD, todos los mensajes son funcionales y están disponibles para mostrarse en las páginas de propiedades de selección múltiple.

Active Directory Domain Services los mensajes siguientes:

-   [**WM \_ ADSPROP \_ NOTIFY \_ APPLY**](wm-adsprop-notify-apply.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ CHANGE**](wm-adsprop-notify-change.md)
-   [**ERROR \_ DE NOTIFICACIÓN DE ADSPROP \_ DE WM \_**](wm-adsprop-notify-error.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ EXIT**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ FOREGROUND**](wm-adsprop-notify-foreground.md)
-   [**PÁGINA \_ DE NOTIFICACIÓN DE ADSPROP DE \_ \_ WMHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**PÁGINA \_ DE NOTIFICACIÓN DE WM ADSPROPINIT \_ \_**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
-   [**NOTIFICACIÓN \_ DE CIERRE DE HOJA DE WM DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY**](wm-dsa-sheet-create-notify.md)

 

 





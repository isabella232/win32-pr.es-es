---
description: Las aplicaciones pueden adaptar mejor su comportamiento al estado de energía actual del equipo mediante el registro de eventos de energía.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registro de eventos de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276829"
---
# <a name="registering-for-power-events"></a>Registro de eventos de energía

Las aplicaciones pueden adaptar mejor su comportamiento al estado de energía actual del equipo mediante el registro de eventos de energía. Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento.

Una aplicación o servicio utiliza la función [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) para registrarse en las notificaciones. Cuando cambia la configuración de energía correspondiente, el sistema envía notificaciones de la siguiente manera:

-   Una aplicación recibe un mensaje de [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) con un *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) y un *lParam* que apunta a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .
-   Un servicio recibe una llamada a la función de devolución de llamada [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) que se registró mediante una llamada a la función [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . El parámetro *lpEventData* enviado a la función de devolución de llamada *HandlerEx* apunta a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

En la estructura de [**\_ configuración POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , el miembro **PowerSetting** contiene el GUID que identifica la notificación y el miembro de **datos** contiene el nuevo valor de la configuración de energía.

Para obtener una lista de los GUID de configuración de energía para las notificaciones que son más útiles para las aplicaciones, consulte [**GUID de configuración de energía**](power-setting-guids.md).

 

 

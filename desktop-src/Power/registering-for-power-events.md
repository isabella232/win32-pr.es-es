---
description: Las aplicaciones pueden adaptar mejor su comportamiento al estado de energía actual del equipo mediante el registro de eventos de energía.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registro de eventos de Power
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143328"
---
# <a name="registering-for-power-events"></a>Registro de eventos de Power

Las aplicaciones pueden adaptar mejor su comportamiento al estado de energía actual del equipo mediante el registro de eventos de energía. Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento.

Una aplicación o servicio usa la [**función RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) para registrarse para recibir notificaciones. Cuando cambia la configuración de energía correspondiente, el sistema envía notificaciones como se muestra a continuación:

-   Una aplicación recibe un [**mensaje \_ WM POWERBROADCAST**](wm-powerbroadcast.md) con *un wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) y *un lParam* que apunta a una [**estructura DE CONFIGURACIÓN DE POWERBROADCAST. \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
-   Un servicio recibe una llamada a la función de devolución de llamada [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) que registró llamando a la [**función RegisterServiceCtrlHandlerEx.**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) El *parámetro lpEventData* enviado a la función de devolución de llamada *HandlerEx* apunta a una [**estructura POWERBROADCAST \_ SETTING.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

En la [**estructura POWERBROADCAST \_ SETTING,**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) el miembro **PowerSetting** contiene el GUID que identifica la notificación y el miembro **Data** contiene el nuevo valor de la configuración de energía.

Para obtener una lista de GUID de configuración de energía para las notificaciones que son más útiles para las aplicaciones, vea GUID [**de configuración de energía**](power-setting-guids.md).

 

 

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
# <a name="registering-for-power-events"></a><span data-ttu-id="fc0a1-103">Registro de eventos de energía</span><span class="sxs-lookup"><span data-stu-id="fc0a1-103">Registering for Power Events</span></span>

<span data-ttu-id="fc0a1-104">Las aplicaciones pueden adaptar mejor su comportamiento al estado de energía actual del equipo mediante el registro de eventos de energía.</span><span class="sxs-lookup"><span data-stu-id="fc0a1-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="fc0a1-105">Una aplicación debe registrarse para cada evento de cambio de energía que pueda afectar a su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="fc0a1-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="fc0a1-106">Una aplicación o servicio utiliza la función [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) para registrarse en las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="fc0a1-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="fc0a1-107">Cuando cambia la configuración de energía correspondiente, el sistema envía notificaciones de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fc0a1-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="fc0a1-108">Una aplicación recibe un mensaje de [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) con un *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) y un *lParam* que apunta a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="fc0a1-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="fc0a1-109">Un servicio recibe una llamada a la función de devolución de llamada [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) que se registró mediante una llamada a la función [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .</span><span class="sxs-lookup"><span data-stu-id="fc0a1-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="fc0a1-110">El parámetro *lpEventData* enviado a la función de devolución de llamada *HandlerEx* apunta a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="fc0a1-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="fc0a1-111">En la estructura de [**\_ configuración POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , el miembro **PowerSetting** contiene el GUID que identifica la notificación y el miembro de **datos** contiene el nuevo valor de la configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="fc0a1-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="fc0a1-112">Para obtener una lista de los GUID de configuración de energía para las notificaciones que son más útiles para las aplicaciones, consulte [**GUID de configuración de energía**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fc0a1-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 

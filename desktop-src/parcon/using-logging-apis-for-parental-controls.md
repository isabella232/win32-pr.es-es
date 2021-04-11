---
description: Uso de las API de registro para controles parentales
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Uso de las API de registro para controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910186"
---
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="5ebc6-103">Uso de las API de registro para controles parentales</span><span class="sxs-lookup"><span data-stu-id="5ebc6-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="5ebc6-104">Informes de actividades (registro)</span><span class="sxs-lookup"><span data-stu-id="5ebc6-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="5ebc6-105">El archivo de encabezado WpcEvent. h contiene definiciones de los campos de cada tipo de evento de actividad predefinido y el tipo personalizado.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="5ebc6-106">En este código de ejemplo se muestran los pasos para registrar un evento de invitación de conversación de mensajería instantánea mediante la API de publicación de ETW:</span><span class="sxs-lookup"><span data-stu-id="5ebc6-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a><span data-ttu-id="5ebc6-107">Registro personalizado</span><span class="sxs-lookup"><span data-stu-id="5ebc6-107">Custom Logging</span></span>

<span data-ttu-id="5ebc6-108">Para que una aplicación extienda los eventos registrados fuera del conjunto de eventos predefinidos o de un tipo personalizado, deberá definir un proveedor para ese en el manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="5ebc6-109">A continuación, se puede importar el canal predeterminado WPC y se pueden registrar eventos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="5ebc6-110">Derechos de registro</span><span class="sxs-lookup"><span data-stu-id="5ebc6-110">Logging Rights</span></span>

<span data-ttu-id="5ebc6-111">El canal de registro de WPC se controla mediante la [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) para proporcionar acceso completo solo a los administradores.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="5ebc6-112">Las cuentas que no son de administrador pueden escribir en el canal pero no tienen acceso de lectura o eliminación.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="5ebc6-113">El acceso al canal es mediante la API ETW.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="5ebc6-114">Detalles del proveedor de registro de controles parentales</span><span class="sxs-lookup"><span data-stu-id="5ebc6-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="5ebc6-115">El proveedor WPC se denomina Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="5ebc6-116">El canal de registro local predeterminado es Microsoft.com/Windows/ParentalControls/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="5ebc6-117">Los archivos de registro se almacenan en la \\ \\ carpeta system32 WPC logs de Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="5ebc6-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="5ebc6-118">Notificación de límite de tiempo inminente de cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="5ebc6-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="5ebc6-119">El sistema de controles parentales desencadenará un evento de advertencia en 15 minutos y de nuevo en 1 minuto antes de cerrar la sesión de un usuario controlado en función de las restricciones de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="5ebc6-120">Las aplicaciones se pueden suscribir a estos eventos, especialmente cuando se ejecutan en el modo de pantalla completa de DirectX, donde no se muestran las notificaciones de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="5ebc6-121">Se proporciona código de ejemplo que muestra cómo suscribirse a los eventos, registrar una función de devolución de llamada y recibir los eventos.</span><span class="sxs-lookup"><span data-stu-id="5ebc6-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ebc6-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ebc6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ebc6-123">Información general sobre las características de extensibilidad de controles parentales</span><span class="sxs-lookup"><span data-stu-id="5ebc6-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="5ebc6-124">**descriptor de datos de evento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ebc6-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="5ebc6-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="5ebc6-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="5ebc6-126">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="5ebc6-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 

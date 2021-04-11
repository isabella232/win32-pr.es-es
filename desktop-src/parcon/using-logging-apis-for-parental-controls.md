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
# <a name="using-logging-apis-for-parental-controls"></a>Uso de las API de registro para controles parentales

### <a name="activity-reporting-logging"></a>Informes de actividades (registro)

El archivo de encabezado WpcEvent. h contiene definiciones de los campos de cada tipo de evento de actividad predefinido y el tipo personalizado. En este código de ejemplo se muestran los pasos para registrar un evento de invitación de conversación de mensajería instantánea mediante la API de publicación de ETW:


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



### <a name="custom-logging"></a>Registro personalizado

Para que una aplicación extienda los eventos registrados fuera del conjunto de eventos predefinidos o de un tipo personalizado, deberá definir un proveedor para ese en el manifiesto de aplicación. A continuación, se puede importar el canal predeterminado WPC y se pueden registrar eventos definidos por la aplicación.

### <a name="logging-rights"></a>Derechos de registro

El canal de registro de WPC se controla mediante la [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) para proporcionar acceso completo solo a los administradores. Las cuentas que no son de administrador pueden escribir en el canal pero no tienen acceso de lectura o eliminación. El acceso al canal es mediante la API ETW.

### <a name="parental-controls-logging-provider-details"></a>Detalles del proveedor de registro de controles parentales

El proveedor WPC se denomina Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}. El canal de registro local predeterminado es Microsoft.com/Windows/ParentalControls/LocalEvents.

Los archivos de registro se almacenan en la \\ \\ carpeta system32 WPC logs de Windows \\ .

### <a name="notification-of-impending-time-limits-logout"></a>Notificación de límite de tiempo inminente de cierre de sesión

El sistema de controles parentales desencadenará un evento de advertencia en 15 minutos y de nuevo en 1 minuto antes de cerrar la sesión de un usuario controlado en función de las restricciones de tiempo. Las aplicaciones se pueden suscribir a estos eventos, especialmente cuando se ejecutan en el modo de pantalla completa de DirectX, donde no se muestran las notificaciones de Windows estándar. Se proporciona código de ejemplo que muestra cómo suscribirse a los eventos, registrar una función de devolución de llamada y recibir los eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las características de extensibilidad de controles parentales](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**descriptor de datos de evento \_ \_**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 

---
description: Uso de las API de registro para los controles parentales
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Uso de las API de registro para los controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 571a24f8bdbf687f8c1975cfc29057035ac56747edc0459682512531194c55a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869067"
---
# <a name="using-logging-apis-for-parental-controls"></a>Uso de las API de registro para los controles parentales

### <a name="activity-reporting-logging"></a>Informe de actividades (registro)

El archivo de encabezado WpcEvent.h contiene definiciones de los campos para cada tipo de evento de actividad predefinido y el tipo personalizado. Este código de ejemplo muestra los pasos para registrar un evento de invitación de conversación de mensajería instantánea mediante la API de publicación de ETW:


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

Para que una aplicación extienda los eventos registrados fuera del conjunto de eventos predefinidos o del tipo personalizado, deberá definir un proveedor para ello en el manifiesto de aplicación. A continuación, se puede importar el canal predeterminado de WPC y, a continuación, se pueden registrar eventos definidos por la aplicación.

### <a name="logging-rights"></a>Derechos de registro

El canal de registro de WPC se controla mediante la [*lista de control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) para proporcionar acceso total solo a los administradores. Las cuentas que no son de administrador pueden escribir en el canal, pero no tienen acceso de lectura o eliminación. El acceso al canal se hace mediante la API ETW.

### <a name="parental-controls-logging-provider-details"></a>Detalles del proveedor de registro de controles parentales

El proveedor de WPC se denomina Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}. El canal de registro local predeterminado es Microsoft.com/Windows/ParentalControls/LocalEvents.

Los archivos de registro se almacenan en Windows \\ carpeta System32 \\ Wpc \\ Logs.

### <a name="notification-of-impending-time-limits-logout"></a>Notificación del cierre de sesión de límites de tiempo impensados

El sistema de controles parentales activa un evento de advertencia a los 15 minutos y de nuevo a 1 minuto antes de cerrar sesión de un usuario controlado en función de las restricciones de tiempo. Las aplicaciones pueden suscribirse a estos eventos, especialmente cuando se ejecutan en modo de pantalla completa de DirectX donde no se muestran Windows notificaciones estándar. Se proporciona código de ejemplo que muestra cómo suscribirse a los eventos, registrar una función de devolución de llamada y recibir los eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las características de extensibilidad de los controles parentales](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**DESCRIPTOR DE \_ DATOS \_ DE EVENTOS**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 

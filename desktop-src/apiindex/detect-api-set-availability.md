---
description: Describe cómo detectar si un conjunto de API específico está disponible en el dispositivo actual.
title: Detección de disponibilidad del conjunto de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2020
ms.locfileid: "104149726"
---
# <a name="detect-api-set-availability"></a>Detección de disponibilidad del conjunto de API

En algunos casos, un nombre de contrato de conjunto de API determinado se puede asignar intencionadamente a un nombre de módulo vacío en algunos dispositivos Windows 10. Los motivos para esto varían, pero un ejemplo común es que una característica costosa en términos de recursos del sistema se puede quitar del sistema operativo Windows cuando se configura para un dispositivo restringido a recursos. Esto supone un reto para que las aplicaciones controlen correctamente las características opcionales en el nivel de API.

El enfoque tradicional para probar si una API de Win32 está disponible es usar [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Sin embargo, estos no son un medio confiable para probar los conjuntos de API debido a la compatibilidad con el [reenvío inverso](api-set-loader-operation.md#reverse-forwarding) en Windows 10. Cuando se aplica el reenvío inverso a una API determinada, **LoadLibrary** o **GetProcAddress** pueden resolverse en un puntero de función válido incluso en los casos en los que se ha quitado la implementación interna. En este caso, el puntero de función va a apuntar a una función de código auxiliar que simplemente devuelve un error.

Para detectar este caso, puede usar la función [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) para consultar la disponibilidad subyacente de una implementación de API determinada. Esta prueba valida que la llamada a esta función dará como resultado la ejecución de una implementación funcional de la API.

En el ejemplo de código siguiente se muestra cómo usar **IsApiSetImplemented** para determinar si la función [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) está disponible en el dispositivo actual antes de llamarla. 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```
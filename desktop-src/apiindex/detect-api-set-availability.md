---
description: Describe cómo detectar si un conjunto de API específico está disponible en el dispositivo actual.
title: Detección de disponibilidad del conjunto de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: cc4e26c6e59cfa0af095b297efb72a52d0be30a89a23d42d169e3bf45e72fd13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896535"
---
# <a name="detect-api-set-availability"></a>Detección de disponibilidad del conjunto de API

En algunos casos, un nombre de contrato de conjunto de API determinado se puede asignar intencionadamente a un nombre de módulo vacío en algunos Windows 10 dispositivos. Las razones de esto varían, pero un ejemplo común es que una característica costosa en términos de recursos del sistema se puede quitar del sistema operativo Windows cuando se configura para un dispositivo con recursos restringidos. Esto supone un desafío para las aplicaciones para controlar correctamente las características opcionales en el nivel de API.

El enfoque tradicional para probar si una API win32 está disponible es usar [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [GetProcAddress.](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Sin embargo, no son un medio confiable para probar conjuntos de API debido a la compatibilidad [con el reenvío](api-set-loader-operation.md#reverse-forwarding) inverso en Windows 10. Cuando se aplica el reenvío inverso a una API determinada, **LoadLibrary** o **GetProcAddress** pueden resolverse como un puntero de función válido incluso en los casos en los que se ha quitado la implementación interna. En este caso, el puntero de función apuntará a una función de código auxiliar que simplemente devuelve un error.

Para detectar este caso, puede usar la función [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) para consultar la disponibilidad subyacente de una implementación de API determinada. Esta prueba valida que la llamada a esta función dará lugar a la ejecución de una implementación funcional de la API.

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
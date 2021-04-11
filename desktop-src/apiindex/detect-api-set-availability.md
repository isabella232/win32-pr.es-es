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
# <a name="detect-api-set-availability"></a><span data-ttu-id="aed00-103">Detección de disponibilidad del conjunto de API</span><span class="sxs-lookup"><span data-stu-id="aed00-103">Detect API set availability</span></span>

<span data-ttu-id="aed00-104">En algunos casos, un nombre de contrato de conjunto de API determinado se puede asignar intencionadamente a un nombre de módulo vacío en algunos dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="aed00-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="aed00-105">Los motivos para esto varían, pero un ejemplo común es que una característica costosa en términos de recursos del sistema se puede quitar del sistema operativo Windows cuando se configura para un dispositivo restringido a recursos.</span><span class="sxs-lookup"><span data-stu-id="aed00-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="aed00-106">Esto supone un reto para que las aplicaciones controlen correctamente las características opcionales en el nivel de API.</span><span class="sxs-lookup"><span data-stu-id="aed00-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="aed00-107">El enfoque tradicional para probar si una API de Win32 está disponible es usar [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="aed00-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="aed00-108">Sin embargo, estos no son un medio confiable para probar los conjuntos de API debido a la compatibilidad con el [reenvío inverso](api-set-loader-operation.md#reverse-forwarding) en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="aed00-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="aed00-109">Cuando se aplica el reenvío inverso a una API determinada, **LoadLibrary** o **GetProcAddress** pueden resolverse en un puntero de función válido incluso en los casos en los que se ha quitado la implementación interna.</span><span class="sxs-lookup"><span data-stu-id="aed00-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="aed00-110">En este caso, el puntero de función va a apuntar a una función de código auxiliar que simplemente devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="aed00-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="aed00-111">Para detectar este caso, puede usar la función [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) para consultar la disponibilidad subyacente de una implementación de API determinada.</span><span class="sxs-lookup"><span data-stu-id="aed00-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="aed00-112">Esta prueba valida que la llamada a esta función dará como resultado la ejecución de una implementación funcional de la API.</span><span class="sxs-lookup"><span data-stu-id="aed00-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="aed00-113">En el ejemplo de código siguiente se muestra cómo usar **IsApiSetImplemented** para determinar si la función [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) está disponible en el dispositivo actual antes de llamarla.</span><span class="sxs-lookup"><span data-stu-id="aed00-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

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
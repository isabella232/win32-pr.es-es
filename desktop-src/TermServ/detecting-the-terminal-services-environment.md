---
title: Detección del entorno de Servicios de Escritorio remoto
description: Para optimizar el rendimiento, es recomendable que las aplicaciones detecten si se ejecutan en una sesión de cliente Servicios de Escritorio remoto.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532152"
---
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="5847c-103">Detección del entorno de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="5847c-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="5847c-104">Para optimizar el rendimiento, es recomendable que las aplicaciones detecten si se ejecutan en una sesión de cliente Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5847c-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="5847c-105">Por ejemplo, cuando una aplicación se ejecuta en una sesión remota, debe eliminar los efectos gráficos innecesarios, tal y como se describe en [efectos gráficos](graphic-effects.md).</span><span class="sxs-lookup"><span data-stu-id="5847c-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="5847c-106">Si el usuario ejecuta la aplicación en un entorno local, no es tan importante que la aplicación optimice su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="5847c-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="5847c-107">En el ejemplo siguiente se muestra una función que devuelve **true** si la aplicación se ejecuta en una sesión remota y **false** si la aplicación se ejecuta en la consola.</span><span class="sxs-lookup"><span data-stu-id="5847c-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="5847c-108">Para obtener más información, vea [vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5847c-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="5847c-109">No debe usar **GetSystemMetrics (SM \_ REMOTESESSION)** para determinar si la aplicación se ejecuta en una sesión remota en Windows 8 y versiones posteriores, o en Windows Server 2012 y versiones posteriores, si la sesión remota también puede usar las mejoras de vGPU de RemoteFX en el protocolo de pantalla remota de Microsoft (RDP).</span><span class="sxs-lookup"><span data-stu-id="5847c-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="5847c-110">En este caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificará la sesión remota como una sesión local.</span><span class="sxs-lookup"><span data-stu-id="5847c-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="5847c-111">La aplicación puede comprobar la siguiente clave del registro para determinar si la sesión es una sesión remota que usa vGPU de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="5847c-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="5847c-112">Si existe una sesión local, esta clave del registro proporciona el identificador de la sesión local.</span><span class="sxs-lookup"><span data-stu-id="5847c-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="5847c-113">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Terminal Server \\ GlassSessionId**</span><span class="sxs-lookup"><span data-stu-id="5847c-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="5847c-114">Si el ID. de la sesión actual en la que se ejecuta la aplicación es el mismo que en la clave del registro, la aplicación se ejecuta en una sesión local.</span><span class="sxs-lookup"><span data-stu-id="5847c-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="5847c-115">Las sesiones identificadas como sesión remota de esta manera incluyen las sesiones remotas que usan vGPU de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="5847c-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="5847c-116">En el siguiente ejemplo de código se muestra este caso.</span><span class="sxs-lookup"><span data-stu-id="5847c-116">The following sample code demonstrates this.</span></span>


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 





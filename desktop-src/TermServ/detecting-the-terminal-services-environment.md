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
# <a name="detecting-the-remote-desktop-services-environment"></a>Detección del entorno de Servicios de Escritorio remoto

Para optimizar el rendimiento, es recomendable que las aplicaciones detecten si se ejecutan en una sesión de cliente Servicios de Escritorio remoto. Por ejemplo, cuando una aplicación se ejecuta en una sesión remota, debe eliminar los efectos gráficos innecesarios, tal y como se describe en [efectos gráficos](graphic-effects.md). Si el usuario ejecuta la aplicación en un entorno local, no es tan importante que la aplicación optimice su comportamiento.

En el ejemplo siguiente se muestra una función que devuelve **true** si la aplicación se ejecuta en una sesión remota y **false** si la aplicación se ejecuta en la consola.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Para obtener más información, vea [vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

No debe usar **GetSystemMetrics (SM \_ REMOTESESSION)** para determinar si la aplicación se ejecuta en una sesión remota en Windows 8 y versiones posteriores, o en Windows Server 2012 y versiones posteriores, si la sesión remota también puede usar las mejoras de vGPU de RemoteFX en el protocolo de pantalla remota de Microsoft (RDP). En este caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificará la sesión remota como una sesión local.

La aplicación puede comprobar la siguiente clave del registro para determinar si la sesión es una sesión remota que usa vGPU de RemoteFX. Si existe una sesión local, esta clave del registro proporciona el identificador de la sesión local.

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Terminal Server \\ GlassSessionId**

Si el ID. de la sesión actual en la que se ejecuta la aplicación es el mismo que en la clave del registro, la aplicación se ejecuta en una sesión local. Las sesiones identificadas como sesión remota de esta manera incluyen las sesiones remotas que usan vGPU de RemoteFX. En el siguiente ejemplo de código se muestra este caso.


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



 

 





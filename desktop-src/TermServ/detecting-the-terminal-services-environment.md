---
title: Detección del Servicios de Escritorio remoto de datos
description: Para optimizar el rendimiento, es una buena práctica que las aplicaciones detecten si se ejecutan en una Servicios de Escritorio remoto cliente.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f54634112b4a6ac3cc1e981421e4a3e33af5e32bae8ab63ec8690f2df12c7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657995"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Detección del Servicios de Escritorio remoto de datos

Para optimizar el rendimiento, es una buena práctica que las aplicaciones detecten si se ejecutan en una Servicios de Escritorio remoto cliente. Por ejemplo, cuando una aplicación se ejecuta en una sesión remota, debe eliminar los efectos gráficos innecesarios, como se describe en [Efectos gráficos](graphic-effects.md). Si el usuario ejecuta la aplicación en un entorno local, no es tan importante para la aplicación optimizar su comportamiento.

En el ejemplo siguiente se muestra una función que devuelve **TRUE si** la aplicación se ejecuta en una sesión remota y **FALSE** si la aplicación se ejecuta en la consola.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Para obtener más información, [vea Vinculación en tiempo de ](run-time-linking-to-wtsapi32-dll.md)ejecución a Wtsapi32.dll.

No debe usar **GetSystemMetrics(SM \_ REMOTESESSION)** para determinar si la aplicación se ejecuta en una sesión remota en Windows 8 y versiones posteriores o Windows Server 2012 y posteriores si la sesión remota también puede usar las mejoras de vGPU de RemoteFX en el Protocolo de visualización remota de Microsoft (RDP). En este caso, **GetSystemMetrics(SM \_ REMOTESESSION)** identificará la sesión remota como una sesión local.

La aplicación puede comprobar la siguiente clave del Registro para determinar si la sesión es una sesión remota que usa RemoteFX vGPU. Si existe una sesión local, esta clave del Registro proporciona el identificador de la sesión local.

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Si el identificador de la sesión actual en la que se ejecuta la aplicación es el mismo que en la clave del Registro, la aplicación se ejecuta en una sesión local. Las sesiones identificadas como sesión remota de esta manera incluyen sesiones remotas que usan RemoteFX vGPU. En el siguiente ejemplo de código se muestra este caso.


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



 

 





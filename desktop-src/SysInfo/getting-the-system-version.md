---
description: En el ejemplo siguiente se usan las funciones del asistente de API de versión para determinar la versión del sistema operativo actual, si se trata de una versión de servidor o cliente y, a continuación, muestra esta información en la consola.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Obtención de la versión del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243981"
---
# <a name="getting-the-system-version"></a>Obtención de la versión del sistema

En el ejemplo siguiente se usan las funciones del asistente de [API](version-helper-apis.md) de versión para determinar la versión del sistema operativo actual, si se trata de una versión de servidor o cliente y, a continuación, muestra esta información en la consola. Si el modo de compatibilidad está en vigor, en el ejemplo se muestra el sistema operativo seleccionado para la [compatibilidad de aplicaciones.](/previous-versions/bb757005(v=msdn.10))

Confiar en la información de versión no es la mejor manera de probar una característica. En su lugar, consulte la documentación de la característica de interés. Para obtener más información sobre las técnicas comunes para la detección de características, vea [Versión del sistema operativo](operating-system-version.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 

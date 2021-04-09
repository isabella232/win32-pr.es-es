---
description: En el ejemplo siguiente se usan las funciones auxiliares de la API de la versión para determinar la versión del sistema operativo actual, si se trata de una versión de servidor o de cliente y, a continuación, se muestra esta información en la consola.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Obtener la versión del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913829"
---
# <a name="getting-the-system-version"></a><span data-ttu-id="5270e-103">Obtener la versión del sistema</span><span class="sxs-lookup"><span data-stu-id="5270e-103">Getting the System Version</span></span>

<span data-ttu-id="5270e-104">En el ejemplo siguiente se usan las [funciones auxiliares](version-helper-apis.md) de la API de la versión para determinar la versión del sistema operativo actual, si se trata de una versión de servidor o de cliente y, a continuación, se muestra esta información en la consola.</span><span class="sxs-lookup"><span data-stu-id="5270e-104">The following example uses the [Version API Helper functions](version-helper-apis.md) to determine the version of the current operating system, if it is a Server or Client release, and then displays this information to the console.</span></span> <span data-ttu-id="5270e-105">Si el modo de compatibilidad está en vigor, el ejemplo muestra el sistema operativo seleccionado para la [compatibilidad de aplicaciones](/previous-versions/bb757005(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="5270e-105">If compatibility mode is in effect, the example displays the operating system selected for [application compatibility](/previous-versions/bb757005(v=msdn.10)).</span></span>

<span data-ttu-id="5270e-106">Confiar en la información de versión no es la mejor manera de probar una característica.</span><span class="sxs-lookup"><span data-stu-id="5270e-106">Relying on version information is not the best way to test for a feature.</span></span> <span data-ttu-id="5270e-107">En su lugar, consulte la documentación de la característica de interés.</span><span class="sxs-lookup"><span data-stu-id="5270e-107">Instead, refer to the documentation for the feature of interest.</span></span> <span data-ttu-id="5270e-108">Para obtener más información sobre técnicas comunes para la detección de características, consulte [versión del sistema operativo](operating-system-version.md).</span><span class="sxs-lookup"><span data-stu-id="5270e-108">For more information on common techniques for feature detection, see [Operating System Version](operating-system-version.md).</span></span>


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



 

 

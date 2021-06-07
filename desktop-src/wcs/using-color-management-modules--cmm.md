---
title: Uso de módulos de administración del color (CMM)
description: Los módulos de administración de colores (CMM) son módulos de código WCS que usan la información de los perfiles de dispositivo para realizar la conversión de colores y la asignación de colores.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Sistema de colores de Windows (WCS),Módulo de administración de colores (CMM)
- WCS (Sistema de colores de Windows),Módulo de administración de colores (CMM)
- administración de colores de imagen,Módulo de administración de colores (CMM)
- administración de colores,Módulo de administración de colores (CMM)
- colors,Módulo de administración de colores (CMM)
- Módulo de administración de colores (CMM)
- CMM (módulo de administración de colores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386904"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="97c18-110">Uso de módulos de administración del color (CMM)</span><span class="sxs-lookup"><span data-stu-id="97c18-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="97c18-111">Los módulos de administración de colores (CMM) son módulos de código WCS que usan la información de los perfiles de dispositivo para realizar la conversión de colores y la asignación de colores.</span><span class="sxs-lookup"><span data-stu-id="97c18-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="97c18-112">Los desarrolladores de aplicaciones no deben tener que implementar CMM.</span><span class="sxs-lookup"><span data-stu-id="97c18-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="97c18-113">Microsoft proporciona el CMM predeterminado.</span><span class="sxs-lookup"><span data-stu-id="97c18-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="97c18-114">Sin embargo, si escribe software que requiere el uso de algoritmos especializados de conversión de colores y asignación de colores, puede crear uno.</span><span class="sxs-lookup"><span data-stu-id="97c18-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="97c18-115">Los puntos de entrada de CMM *no son* funciones de API y las aplicaciones no deben llamar a ellos.</span><span class="sxs-lookup"><span data-stu-id="97c18-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="97c18-116">Cuando se instalan las CMM, el programa de instalación los registra en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="97c18-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="97c18-117">Las aplicaciones pueden enumerar las CMM registradas y seleccionar una mediante la [**función SelectCMM.**](/windows/win32/api/icm/nf-icm-selectcmm)</span><span class="sxs-lookup"><span data-stu-id="97c18-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="97c18-118">En la siguiente aplicación de ejemplo se muestra cómo enumerar todas las CMM registradas.</span><span class="sxs-lookup"><span data-stu-id="97c18-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 





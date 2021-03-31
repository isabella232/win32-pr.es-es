---
title: Detectando el estado de la instalación del programa de instalación de Windows Media
description: Detectando el estado de la instalación del programa de instalación de Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, detectar el estado de la instalación
- Windows Media Player, estado de la instalación
- Windows Media Player, redistribuir software
- Windows Media Player, redistribución de software
- detección del estado de la instalación
- Estado de la instalación
- redistribuir software
- redistribución de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419070"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="5b9b5-111">Detectando el estado de la instalación del programa de instalación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="5b9b5-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="5b9b5-112">El siguiente código se puede utilizar con los paquetes de redistribución de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5b9b5-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="5b9b5-113">El estado de la instalación se almacena en la entrada del registro **InstallResult** en la siguiente subclave:</span><span class="sxs-lookup"><span data-stu-id="5b9b5-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="5b9b5-114">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ setup**</span><span class="sxs-lookup"><span data-stu-id="5b9b5-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="5b9b5-115">La entrada del registro **InstallResult** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b9b5-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="5b9b5-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="5b9b5-116">Name</span></span>              | <span data-ttu-id="5b9b5-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b9b5-117">Type</span></span>           | <span data-ttu-id="5b9b5-118">Value</span><span class="sxs-lookup"><span data-stu-id="5b9b5-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9b5-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="5b9b5-119">**InstallResult**</span></span> | <span data-ttu-id="5b9b5-120">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="5b9b5-120">**REG\_DWORD**</span></span> | <span data-ttu-id="5b9b5-121">Un **valor HRESULT** que indica si la instalación de Windows Media Player realizó correctamente y si es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="5b9b5-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="5b9b5-122">Este es un ejemplo de código de C++ que se puede incorporar en una aplicación de configuración de llamada.</span><span class="sxs-lookup"><span data-stu-id="5b9b5-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="5b9b5-123">Este código establecerá las `fSuccess` `fRebootNeeded` variables y en **true** o **false**, según corresponda, en función del valor **HRESULT** escrito por el programa de instalación de Windows Media Player en el paquete de redistribución de componentes.</span><span class="sxs-lookup"><span data-stu-id="5b9b5-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="5b9b5-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b9b5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b9b5-125">**Redistribuir el software de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="5b9b5-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 





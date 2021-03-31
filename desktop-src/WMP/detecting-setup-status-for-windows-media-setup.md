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
# <a name="detecting-setup-status-for-windows-media-setup"></a>Detectando el estado de la instalación del programa de instalación de Windows Media

El siguiente código se puede utilizar con los paquetes de redistribución de Windows Media Player. El estado de la instalación se almacena en la entrada del registro **InstallResult** en la siguiente subclave:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ setup**

La entrada del registro **InstallResult** tiene el formato siguiente.



| Nombre              | Tipo           | Value                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **\_valor DWORD reg** | Un **valor HRESULT** que indica si la instalación de Windows Media Player realizó correctamente y si es necesario reiniciar. |



 

Este es un ejemplo de código de C++ que se puede incorporar en una aplicación de configuración de llamada. Este código establecerá las `fSuccess` `fRebootNeeded` variables y en **true** o **false**, según corresponda, en función del valor **HRESULT** escrito por el programa de instalación de Windows Media Player en el paquete de redistribución de componentes.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir el software de Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 





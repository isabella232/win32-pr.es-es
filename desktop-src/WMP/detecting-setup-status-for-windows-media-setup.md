---
title: Detección del estado de instalación de Windows instalación de medios
description: Detección del estado de instalación de Windows instalación de medios
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Reproductor de Windows Media, detectar el estado de instalación
- Reproductor de Windows Media,estado de instalación
- Reproductor de Windows Media, redistribuir software
- Reproductor de Windows Media, redistribución de software
- detectar el estado de configuración
- estado de configuración
- redistribuir software
- redistribución de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340904"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Detección del estado de instalación de Windows instalación de medios

El código siguiente se puede usar con los paquetes Reproductor de Windows Media redistribución. El estado de instalación se almacena en la entrada del Registro **InstallResult** en la subclave siguiente:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Setup**

La **entrada del Registro InstallResult** tiene el siguiente formulario.



| Nombre              | Tipo           | Valor                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | HRESULT **que** indica si la Reproductor de Windows Media se ha realizado correctamente y si es necesario reiniciar. |



 

Este es un ejemplo de código de C++ que se podría incorporar a una aplicación de instalación de llamada. Este código establecerá las variables y en true o false, según corresponda, en función del valor HRESULT escrito por Reproductor de Windows Media setup en el paquete `fSuccess` `fRebootNeeded` de redistribución de componentes.   


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

[**Redistribuir Reproductor de Windows Media Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 





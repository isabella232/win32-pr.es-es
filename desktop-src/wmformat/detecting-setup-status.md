---
title: Detección del estado de la instalación
description: Detección del estado de la instalación
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- SDK de Windows Media Format, redistribución de software
- Advanced Systems Format (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- SDK de Windows Media Format, redistribución
- Advanced Systems Format (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, detección del estado de la instalación
- redistribución, detección del estado de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779753"
---
# <a name="detecting-setup-status"></a>Detección del estado de la instalación

Cuando el ejecutable de redistribución se ejecuta en un equipo, registra su estado de instalación en el registro como un valor **HRESULT** . El estado de la instalación se almacena en la entrada del registro **InstallResult** en la siguiente subclave:

**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ setup**

La entrada del registro **InstallResult** tiene el formato siguiente.



| Nombre              | Tipo           | Value                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **\_valor DWORD reg** | Un **valor HRESULT** que indica si la instalación de Windows Media Player realizó correctamente y si es necesario reiniciar. |



 

El código siguiente establecerá las variables *fSucess* y *fRebootNeeded* en **true** o **false**, según corresponda, en función del valor **HRESULT** escrito por el programa de instalación de Windows Media en el paquete de redistribución de componentes.


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribución de software**](software-redistribution.md)
</dt> </dl>

 

 





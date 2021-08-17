---
title: Detección del estado de la instalación
description: Detección del estado de la instalación
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows SDK de formato multimedia, redistribución de software
- Formato de sistemas avanzados (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- Windows SDK de formato multimedia, redistribución
- Formato de sistemas avanzados (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, detección del estado de instalación
- redistribution,detecting setup status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250ab87fd81592b868e1dbf13106577f83e680796310aff246f0c1483fa847cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931406"
---
# <a name="detecting-setup-status"></a>Detección del estado de la instalación

Cuando el ejecutable de redistribución se ejecuta en un equipo, registra su estado de instalación en el Registro como **un valor HRESULT.** El estado de instalación se almacena en la entrada del Registro **InstallResult** en la subclave siguiente:

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Setup**

La **entrada del Registro InstallResult** tiene el siguiente formulario.



| Nombre              | Tipo           | Value                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **REG \_ DWORD** | HRESULT **que** indica si la Reproductor de Windows Media se ha realizado correctamente y si es necesario reiniciar. |



 

El código siguiente establecerá las variables *fSucess* y *fRebootNeeded* en **True** o **False,** según corresponda, en función del **valor HRESULT** escrito por el programa de instalación de Windows Media en el paquete de redistribución de componentes.


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

 

 





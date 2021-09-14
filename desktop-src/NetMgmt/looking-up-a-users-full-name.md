---
title: Buscar el nombre completo de un usuario
description: Los equipos se pueden organizar en un dominio, que es una colección de redes de equipos. El administrador de dominio mantiene información centralizada de cuentas de grupo y usuario.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069402"
---
# <a name="looking-up-a-users-full-name"></a>Buscar el nombre completo de un usuario

Los equipos se pueden organizar en un *dominio*, que es una colección de redes de equipos. El administrador de dominio mantiene información centralizada de cuentas de grupo y usuario.

Para buscar el nombre completo de un usuario, dados el nombre de usuario y el nombre de dominio:

-   Convierta el nombre de usuario y el nombre de dominio en Unicode, si aún no son cadenas Unicode.
-   Busque el nombre de equipo del controlador de dominio (DC) mediante una llamada a [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Busque el nombre de usuario en el equipo del controlador de dominio mediante una llamada [**a NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Convierta el nombre de usuario completo en ANSI, a menos que el programa espere trabajar con cadenas Unicode.

El código de ejemplo siguiente es una función (GetFullName) que toma un nombre de usuario y un nombre de dominio en los dos primeros argumentos y devuelve el nombre completo del usuario en el tercer argumento.


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 





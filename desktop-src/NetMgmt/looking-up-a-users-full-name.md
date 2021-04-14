---
title: Buscar el nombre completo de un usuario
description: Los equipos pueden organizarse en un dominio, que es una colección de redes de equipos. El administrador del dominio mantiene la información centralizada de la cuenta de usuario y de grupo.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665669"
---
# <a name="looking-up-a-users-full-name"></a>Buscar el nombre completo de un usuario

Los equipos pueden organizarse en un *dominio*, que es una colección de redes de equipos. El administrador del dominio mantiene la información centralizada de la cuenta de usuario y de grupo.

Para buscar el nombre completo de un usuario, dado el nombre de usuario y el nombre de dominio:

-   Convierta el nombre de usuario y el nombre de dominio a Unicode, si aún no son cadenas Unicode.
-   Busca el nombre del equipo del controlador de dominio (DC) mediante una llamada a [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Para buscar el nombre de usuario en el equipo DC, llame a [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Convierta el nombre de usuario completo en ANSI, a menos que el programa esté esperando trabajar con cadenas Unicode.

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



 

 





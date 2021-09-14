---
title: Forzar a un usuario a cambiar la contraseña de inicio de sesión
description: En este ejemplo de código se muestra cómo forzar a un usuario a cambiar la contraseña de inicio de sesión en el siguiente inicio de sesión mediante las funciones NetUserGetInfo y NetUserSetInfo y la estructura USER \_ INFO \_ 3.
ms.assetid: 828f5d72-3e19-4b65-a1db-ac702fd4cfde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3d0910f77c2553a55a53f1393aae5c9535982
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069413"
---
# <a name="forcing-a-user-to-change-the-logon-password"></a>Forzar a un usuario a cambiar la contraseña de inicio de sesión

En este ejemplo de código se muestra cómo forzar a un usuario a cambiar la contraseña de inicio de sesión en el siguiente inicio de sesión mediante las funciones [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) y [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) y la [**estructura USER INFO \_ \_ 3.**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) Tenga en cuenta que a Windows XP, se recomienda usar la estructura [**\_ USER INFO \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) en su lugar.

Establezca el **miembro usri3 \_ password \_ expired** de la **estructura USER INFO \_ \_ 3** en un valor distinto de cero mediante el siguiente fragmento de código:


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

#define USERNAME L"your_user_name"
#define SERVER L"\\\\server"

void main( void )
{
    PUSER_INFO_3 pUsr = NULL;
    NET_API_STATUS netRet = 0;
    DWORD dwParmError = 0;
 //
 // First, retrieve the user information at level 3. This is 
 // necessary to prevent resetting other user information when 
 // the NetUserSetInfo call is made.
 //
   netRet = NetUserGetInfo( SERVER, USERNAME, 3, (LPBYTE *)&pUsr);

   if( netRet == NERR_Success )
   {
     //
     // The function was successful; set the usri3_password_expired value to 
     // a nonzero value. Call the NetUserSetInfo function.
     //
        pUsr->usri3_password_expired = TRUE;
        netRet = NetUserSetInfo( SERVER, USERNAME, 3, (LPBYTE)pUsr, &dwParmError);
    //
    // A zero return indicates success. 
    // If the return value is ERROR_INVALID_PARAMETER, 
    //  the dwParmError parameter will contain a value indicating the 
    //  invalid parameter within the user_info_3 structure. These values 
    //  are defined in the lmaccess.h file.
    //
        if( netRet == NERR_Success )
            printf("User %S will need to change password at next logon", USERNAME);
        else printf("Error %d occurred. Parm Error %d returned.\n", netRet, dwParmError);
    //
    // Must free the buffer returned by NetUserGetInfo.
    //
        NetApiBufferFree( pUsr);
    }
    else printf("NetUserGetInfo failed: %d\n", netRet);
}
```



 

 





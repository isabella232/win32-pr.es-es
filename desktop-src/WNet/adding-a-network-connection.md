---
title: Agregar una conexión de red
description: Para realizar una conexión a un recurso de red descrito por una estructura NETRESOURCE, una aplicación puede llamar a WNetAddConnection2, WNetAddConnection3 o a la función WNetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8298216ab277c5f0ec4a0db8c4d6d1b6c592a8b643e6c30de96731ae2a32632b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053393"
---
# <a name="adding-a-network-connection"></a>Agregar una conexión de red

Para realizar una conexión a un recurso de red descrito por una estructura [**NETRESOURCE,**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) una aplicación puede llamar a [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)o a la función [**WNetUseConnection.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) En el ejemplo siguiente se muestra el uso de la **función WNetAddConnection2.**

El ejemplo de código llama a la función **WNetAddConnection2,** especificando que el sistema debe actualizar el perfil del usuario con la información, creando una conexión "recordada" o persistente. El ejemplo llama a un controlador de errores definido por la aplicación para procesar errores y a la [**función TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



La [**función WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) es compatible con versiones anteriores de Windows para grupos de trabajo. Las nuevas aplicaciones deben llamar a [**la función WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o [**a la función WNetAddConnection3.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)

Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, vea [Recuperación de errores de red.](retrieving-network-errors.md)

 

 
---
title: Cancelación de una conexión de red
description: Para cancelar una conexión a un recurso de red, una aplicación puede llamar a la función WNetCancelConnection2, como se muestra en el ejemplo siguiente.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566925"
---
# <a name="canceling-a-network-connection"></a>Cancelación de una conexión de red

Para cancelar una conexión a un recurso de red, una aplicación puede llamar a la función [**WNetCancelConnection2,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) como se muestra en el ejemplo siguiente.

La llamada a **WNetCancelConnection2** especifica que una conexión de red ya no debe ser persistente. El ejemplo llama a un controlador de errores definido por la aplicación para procesar errores y a la [**función TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



La [**función WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) es compatible con versiones anteriores de Windows para grupos de trabajo. Para las nuevas aplicaciones, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, vea [Recuperación de errores de red.](retrieving-network-errors.md)

 

 
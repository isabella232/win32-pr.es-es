---
title: Recuperar el nombre de conexión
description: Para recuperar el nombre del recurso de red asociado a un dispositivo local, una aplicación puede llamar a la función WNetGetConnection, como se muestra en el ejemplo siguiente.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264a7352fb10139df538d5803fc94966b276fa334f2e4ef5f2c0799e1c32c4cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566832"
---
# <a name="retrieving-the-connection-name"></a>Recuperar el nombre de conexión

Para recuperar el nombre del recurso de red asociado a un dispositivo local, una aplicación puede llamar a la función [**WNetGetConnection,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) como se muestra en el ejemplo siguiente.

En el ejemplo siguiente se llama a un controlador de errores definido por la aplicación para procesar errores y a la [**función TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.


```C++
TCHAR szDeviceName[80]; 
DWORD dwResult, cchBuff = sizeof(szDeviceName); 
 
// Call the WNetGetConnection function.
//
dwResult = WNetGetConnection(_T("z:"), 
    szDeviceName, 
    &cchBuff); 
 
switch (dwResult) 
{ 
    //
    // Print the connection name or process errors.
    //
    case NO_ERROR: 
        printf("Connection name: %s\n", szDeviceName); 
        break; 
    //
    // The device is not a redirected device.
    //
    case ERROR_NOT_CONNECTED: 
        printf("Device z: not connected.\n"); 
        break;
    //
    // The device is not currently connected, but it is a persistent connection.
    //
    case ERROR_CONNECTION_UNAVAIL: 
        printf("Connection unavailable.\n"); 
        break;
    //
    // Handle the error.
    //
    default: 
        printf("WNetGetConnection failed.\n"); 
}
```



Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, vea [Retrieving Network Errors](retrieving-network-errors.md).

 

 
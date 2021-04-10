---
title: Recuperar el nombre de la conexión
description: Para recuperar el nombre del recurso de red asociado a un dispositivo local, una aplicación puede llamar a la función WNetGetConnection, tal y como se muestra en el ejemplo siguiente.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac84aec3c6aafb8a5113ea29251247a1de35aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149436"
---
# <a name="retrieving-the-connection-name"></a>Recuperar el nombre de la conexión

Para recuperar el nombre del recurso de red asociado a un dispositivo local, una aplicación puede llamar a la función [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) , tal y como se muestra en el ejemplo siguiente.

En el ejemplo siguiente se llama a un controlador de errores definido por la aplicación para procesar errores y la función [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.


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



Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, consulte [recuperar errores de red](retrieving-network-errors.md).

 

 
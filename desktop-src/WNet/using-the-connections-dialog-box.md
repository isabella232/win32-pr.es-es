---
title: Usar el cuadro de diálogo Conexiones
description: La función WNetConnectionDialog crea un cuadro de diálogo que permite al usuario examinar y conectarse a los recursos de red.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361718"
---
# <a name="using-the-connections-dialog-box"></a>Usar el cuadro de diálogo Conexiones

La [**función WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crea un cuadro de diálogo que permite al usuario examinar y conectarse a los recursos de red. También puede llamar a la función [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) para crear un cuadro de diálogo de conexiones. **WNetConnectionDialog1** requiere una [**estructura CONNECTDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa)

La [**función WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crea un cuadro de diálogo que permite al usuario desconectarse de los recursos de red.

En el ejemplo de código siguiente se muestra cómo llamar a la **función WNetConnectionDialog** para crear un cuadro de diálogo que muestre los recursos de disco. Si se produce un error en la llamada, el ejemplo llama a un controlador de errores definido por la aplicación.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, vea [Retrieving Network Errors](retrieving-network-errors.md).

 

 
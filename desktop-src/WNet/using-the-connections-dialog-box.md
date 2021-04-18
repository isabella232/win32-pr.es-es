---
title: Usar el cuadro de diálogo conexiones
description: La función WNetConnectionDialog crea un cuadro de diálogo que permite al usuario examinar y conectarse a los recursos de red.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359156"
---
# <a name="using-the-connections-dialog-box"></a>Usar el cuadro de diálogo conexiones

La función [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crea un cuadro de diálogo que permite al usuario examinar y conectarse a los recursos de red. También puede llamar a la función [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) para crear un cuadro de diálogo de conexiones. **WNetConnectionDialog1** requiere una estructura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .

La función [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crea un cuadro de diálogo que permite al usuario desconectarse de los recursos de red.

En el ejemplo de código siguiente se muestra cómo llamar a la función **WNetConnectionDialog** para crear un cuadro de diálogo que muestra los recursos de disco. Si se produce un error en la llamada, el ejemplo llama a un controlador de errores definido por la aplicación.


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



Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, consulte [recuperar errores de red](retrieving-network-errors.md).

 

 
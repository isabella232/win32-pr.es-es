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
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="dd9e5-103">Usar el cuadro de diálogo conexiones</span><span class="sxs-lookup"><span data-stu-id="dd9e5-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="dd9e5-104">La función [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crea un cuadro de diálogo que permite al usuario examinar y conectarse a los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="dd9e5-105">También puede llamar a la función [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) para crear un cuadro de diálogo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="dd9e5-106">**WNetConnectionDialog1** requiere una estructura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .</span><span class="sxs-lookup"><span data-stu-id="dd9e5-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="dd9e5-107">La función [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crea un cuadro de diálogo que permite al usuario desconectarse de los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="dd9e5-108">En el ejemplo de código siguiente se muestra cómo llamar a la función **WNetConnectionDialog** para crear un cuadro de diálogo que muestra los recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="dd9e5-109">Si se produce un error en la llamada, el ejemplo llama a un controlador de errores definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-109">If the call fails, the sample calls an application-defined error handler.</span></span>


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



<span data-ttu-id="dd9e5-110">Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, consulte [recuperar errores de red](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="dd9e5-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 
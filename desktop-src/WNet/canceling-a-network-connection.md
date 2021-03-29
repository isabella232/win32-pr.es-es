---
title: Cancelar una conexión de red
description: Para cancelar una conexión a un recurso de red, una aplicación puede llamar a la función WNetCancelConnection2, tal y como se muestra en el ejemplo siguiente.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904747"
---
# <a name="canceling-a-network-connection"></a><span data-ttu-id="53516-103">Cancelar una conexión de red</span><span class="sxs-lookup"><span data-stu-id="53516-103">Canceling a Network Connection</span></span>

<span data-ttu-id="53516-104">Para cancelar una conexión a un recurso de red, una aplicación puede llamar a la función [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="53516-104">To cancel a connection to a network resource, an application can call the [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) function, as shown in the following example.</span></span>

<span data-ttu-id="53516-105">La llamada a **WNetCancelConnection2** especifica que una conexión de red ya no debe ser persistente.</span><span class="sxs-lookup"><span data-stu-id="53516-105">The call to **WNetCancelConnection2** specifies that a network connection should no longer be persistent.</span></span> <span data-ttu-id="53516-106">En el ejemplo se llama a un controlador de errores definido por la aplicación para procesar errores y la función [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.</span><span class="sxs-lookup"><span data-stu-id="53516-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


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



<span data-ttu-id="53516-107">La función [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) se admite por compatibilidad con versiones anteriores de Windows para grupos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="53516-107">The [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="53516-108">Para las nuevas aplicaciones, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span><span class="sxs-lookup"><span data-stu-id="53516-108">For new applications, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

<span data-ttu-id="53516-109">Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, consulte [recuperar errores de red](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="53516-109">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 
---
title: Recuperar el nombre de usuario
description: Para recuperar el nombre del usuario asociado con un dispositivo local conectado a un recurso de red o con el nombre de una red, una aplicación puede llamar a la función WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271314"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="000c8-103">Recuperar el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="000c8-103">Retrieving the User Name</span></span>

<span data-ttu-id="000c8-104">Para recuperar el nombre del usuario asociado con un dispositivo local conectado a un recurso de red o con el nombre de una red, una aplicación puede llamar a la función [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="000c8-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="000c8-105">En el ejemplo siguiente se usa el nombre del dispositivo para recuperar el nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="000c8-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="000c8-106">En el ejemplo se llama a un controlador de errores definido por la aplicación para procesar errores y la función [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) para imprimir.</span><span class="sxs-lookup"><span data-stu-id="000c8-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



<span data-ttu-id="000c8-107">Para obtener más información sobre el uso de un controlador de errores definido por la aplicación, consulte [recuperar errores de red](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="000c8-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 
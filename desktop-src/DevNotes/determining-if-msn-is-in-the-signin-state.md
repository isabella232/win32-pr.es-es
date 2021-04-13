---
description: En el ejemplo de código siguiente se muestra el uso de un objeto mutex para determinar si MSN Explorer ha iniciado sesión.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinar si MSN está en el estado de inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539123"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="4cc40-103">Determinar si MSN está en el estado de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="4cc40-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="4cc40-104">En el ejemplo de código siguiente se muestra el uso de un objeto mutex para determinar si MSN Explorer ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4cc40-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="4cc40-105">Cuando haya terminado de usar el identificador, asegúrese de llamar a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="4cc40-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="4cc40-106">Este objeto mutex está disponible para su uso en la comprobación de MSN Explorer 7. Estado de inicio de sesión *x* .</span><span class="sxs-lookup"><span data-stu-id="4cc40-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="4cc40-107">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4cc40-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 

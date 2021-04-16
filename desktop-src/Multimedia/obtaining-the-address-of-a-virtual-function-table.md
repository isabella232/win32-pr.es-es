---
title: Obtener la dirección de una tabla de función virtual
description: Obtener la dirección de una tabla de función virtual
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532110"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="9ca51-103">Obtener la dirección de una tabla de función virtual</span><span class="sxs-lookup"><span data-stu-id="9ca51-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="9ca51-104">En una aplicación escrita en el lenguaje de programación C, puede recuperar la dirección de la estructura **IAVIStreamVtbl** mediante la función NewBall.</span><span class="sxs-lookup"><span data-stu-id="9ca51-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="9ca51-105">Esta función devuelve la dirección de una estructura que contiene un puntero a **IAVIStreamVtbl**.</span><span class="sxs-lookup"><span data-stu-id="9ca51-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="9ca51-106">La información que sigue al puntero **IAVIStreamVtbl** especifica los datos que AVIBall usa internamente.</span><span class="sxs-lookup"><span data-stu-id="9ca51-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="9ca51-107">El controlador de flujo puede anexar su propia información después del puntero **IAVIStreamVtbl** .</span><span class="sxs-lookup"><span data-stu-id="9ca51-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="9ca51-108">Esta información se devuelve en las llamadas subsiguientes al controlador de flujo.</span><span class="sxs-lookup"><span data-stu-id="9ca51-108">This information is returned in subsequent calls to your stream handler.</span></span>


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 





---
title: " in, String y out, prototipo de cadena"
description: 'El prototipo de función siguiente usa dos parámetros: \ in, String \ Parameter y un parámetro \ out, String \.'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995570"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="671bf-103">\[in, String \] y \[ out, prototipo de cadena \]</span><span class="sxs-lookup"><span data-stu-id="671bf-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="671bf-104">El prototipo de función siguiente usa dos parámetros: \[ [**en**](/windows/desktop/Midl/in), parámetro de [**cadena**](/windows/desktop/Midl/string) \] y un \[ parámetro [**out**](/windows/desktop/Midl/out-idl)de **cadena** \] .</span><span class="sxs-lookup"><span data-stu-id="671bf-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="671bf-105">El primer parámetro es \[ solo [**en**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="671bf-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="671bf-106">Esta cadena de entrada solo se transmite desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="671bf-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="671bf-107">El servidor lo utiliza como base para su posterior procesamiento.</span><span class="sxs-lookup"><span data-stu-id="671bf-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="671bf-108">La cadena no se modifica y el cliente no la necesita, por lo que no tiene que devolverse al cliente.</span><span class="sxs-lookup"><span data-stu-id="671bf-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="671bf-109">El segundo parámetro, que representa la respuesta del médico, \[ solo está [**fuera**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="671bf-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="671bf-110">Esta cadena de respuesta solo se transmite desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="671bf-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="671bf-111">Se proporciona el tamaño de asignación para que el código auxiliar del servidor pueda asignar memoria para él.</span><span class="sxs-lookup"><span data-stu-id="671bf-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="671bf-112">Puesto que *pszOutput* es un puntero de \[ [**referencia**](/windows/desktop/Midl/ref) \] , el cliente debe tener suficiente memoria asignada para la cadena antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="671bf-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="671bf-113">La cadena de respuesta se escribe en esta área de memoria cuando se devuelve el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="671bf-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 
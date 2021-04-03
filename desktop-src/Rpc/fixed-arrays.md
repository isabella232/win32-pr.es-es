---
title: Matrices fijas
description: Si la interfaz especifica una matriz con un número específico de elementos como parámetro, se usa una matriz fija. Al usar MIDL, se definen matrices fijas de la misma manera que se definen en C. Especifique el tipo, el nombre y el tamaño de la matriz.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776968"
---
# <a name="fixed-arrays"></a><span data-ttu-id="82538-104">Matrices fijas</span><span class="sxs-lookup"><span data-stu-id="82538-104">Fixed Arrays</span></span>

<span data-ttu-id="82538-105">Si la interfaz especifica una matriz con un número específico de elementos como parámetro, se usa una matriz fija.</span><span class="sxs-lookup"><span data-stu-id="82538-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="82538-106">Al usar MIDL, se definen matrices fijas de la misma manera que se definen en C. Especifique el tipo, el nombre y el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="82538-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="82538-107">En el ejemplo siguiente se muestra cómo definir una matriz fija.</span><span class="sxs-lookup"><span data-stu-id="82538-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="82538-108">Cuando un programa cliente pasa una matriz fija a un programa de servidor, el código auxiliar del cliente envía toda la matriz al código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="82538-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="82538-109">El código auxiliar del servidor asigna memoria a la matriz y almacena los datos de la matriz que recibe a través de la red en la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="82538-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="82538-110">A continuación, pasa la matriz al procedimiento remoto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="82538-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="82538-111">El servidor puede modificar los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="82538-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="82538-112">Cuando finaliza el procedimiento remoto, el código auxiliar del servidor envía el contenido de la matriz de vuelta al cliente.</span><span class="sxs-lookup"><span data-stu-id="82538-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="82538-113">El código auxiliar del cliente copia los datos recibidos del código auxiliar del servidor en la matriz original.</span><span class="sxs-lookup"><span data-stu-id="82538-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="82538-114">Después, el programa cliente puede utilizar los datos como si hubiera recibido los datos de una llamada a procedimiento local.</span><span class="sxs-lookup"><span data-stu-id="82538-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 





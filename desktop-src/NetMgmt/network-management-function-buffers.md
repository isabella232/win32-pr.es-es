---
title: Búferes de función de administración de red
description: La biblioteca en tiempo de ejecución de RPC controla los búferes que requieren las funciones de administración de red de recuperación de datos de 32 bits como se indica a continuación.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268917"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="a6b44-103">Búferes de función de administración de red</span><span class="sxs-lookup"><span data-stu-id="a6b44-103">Network Management Function Buffers</span></span>

<span data-ttu-id="a6b44-104">La biblioteca en tiempo de ejecución de RPC controla los búferes que requieren las funciones de administración de red de recuperación de datos de 32 bits de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a6b44-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="a6b44-105">**Enviar datos al servidor** (datos especificados por \[ \] los parámetros in).</span><span class="sxs-lookup"><span data-stu-id="a6b44-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="a6b44-106">El autor de la llamada debe asignar y desasignar el búfer de la estructura (o estructuras) de información pertinente y pasar una variable de puntero a la función.</span><span class="sxs-lookup"><span data-stu-id="a6b44-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="a6b44-107">El autor de la llamada no necesita especificar la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="a6b44-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="a6b44-108">Ejemplo: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="a6b44-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="a6b44-109">**Recuperar datos del servidor** (datos especificados por \[ parámetros out \] ).</span><span class="sxs-lookup"><span data-stu-id="a6b44-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="a6b44-110">El sistema asigna el búfer para la información devuelta.</span><span class="sxs-lookup"><span data-stu-id="a6b44-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="a6b44-111">El llamador debe pasar una variable de puntero a la función en la entrada.</span><span class="sxs-lookup"><span data-stu-id="a6b44-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="a6b44-112">El puntero recibe la dirección del búfer asignado por el sistema que contiene la información devuelta, si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="a6b44-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="a6b44-113">Esto simplifica el código de llamada, porque el autor de la llamada no necesita calcular el tamaño del búfer o cambiar el tamaño del búfer y volver a emitir la función.</span><span class="sxs-lookup"><span data-stu-id="a6b44-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="a6b44-114">Cuando el autor de la llamada ha terminado de procesar la información devuelta, debe liberar la memoria asignada por el sistema mediante una llamada a la función [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) .</span><span class="sxs-lookup"><span data-stu-id="a6b44-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="a6b44-115">Para obtener más información sobre cómo especificar los tamaños de búfer, vea [longitud de búfer de funciones de administración de red](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="a6b44-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="a6b44-116">Ejemplo: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="a6b44-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 





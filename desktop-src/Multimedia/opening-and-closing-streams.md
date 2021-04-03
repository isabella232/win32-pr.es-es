---
title: Abrir y cerrar secuencias
description: Abrir y cerrar secuencias
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream función)
- AVIStreamRelease función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075438"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="559be-105">Abrir y cerrar secuencias</span><span class="sxs-lookup"><span data-stu-id="559be-105">Opening and Closing Streams</span></span>

<span data-ttu-id="559be-106">Abrir flujos de datos es similar a abrir archivos.</span><span class="sxs-lookup"><span data-stu-id="559be-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="559be-107">Puede abrir una secuencia mediante la función [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) .</span><span class="sxs-lookup"><span data-stu-id="559be-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="559be-108">Esta función crea una interfaz de flujo, coloca un identificador de la secuencia en la interfaz y devuelve un puntero a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="559be-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="559be-109">**AVIFileGetStream** también mantiene un recuento de referencias de las aplicaciones que han abierto una secuencia, pero no de las que la han cerrado.</span><span class="sxs-lookup"><span data-stu-id="559be-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="559be-110">Si desea tener acceso a un solo flujo en un archivo, puede abrir el archivo y la secuencia mediante la función [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) .</span><span class="sxs-lookup"><span data-stu-id="559be-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="559be-111">Esta función combina las operaciones y los argumentos de función de las funciones [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) y **AVIFileGetStream** .</span><span class="sxs-lookup"><span data-stu-id="559be-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="559be-112">Para tener acceso a más de un flujo en un archivo, use **AVIFileOpen** una vez seguido de varias llamadas a **AVIFileGetStream**.</span><span class="sxs-lookup"><span data-stu-id="559be-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="559be-113">Puede incrementar el recuento de referencias de una secuencia mediante la función [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) para mantener abierta una secuencia cuando se usa una función que normalmente cerraría la secuencia.</span><span class="sxs-lookup"><span data-stu-id="559be-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="559be-114">Puede cerrar una secuencia mediante la función [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="559be-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="559be-115">Esta función reduce el recuento de referencias de la secuencia y la cierra cuando el recuento de referencias llega a cero.</span><span class="sxs-lookup"><span data-stu-id="559be-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="559be-116">Las aplicaciones deben equilibrar el recuento de referencias incluyendo una llamada a **AVIStreamRelease** para cada uso de la función [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** o **AVIStreamOpenFromFile** .</span><span class="sxs-lookup"><span data-stu-id="559be-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="559be-117">Cuando se libera una secuencia que se ha abierto con **AVIStreamOpenFromFile**, AVIFile cierra el archivo que contiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="559be-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="559be-118">Si la aplicación libera un archivo que tiene flujos de datos abiertos, AVIFile no cerrará los flujos hasta que se liberen todas las secuencias.</span><span class="sxs-lookup"><span data-stu-id="559be-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 





---
description: Proporciona una breve introducción a algunos tipos de situaciones de saturación del búfer y ofrece algunas ideas y recursos para ayudarle a evitar la creación de nuevos riesgos y a mitigar los existentes.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitar saturaciones del búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668045"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="452cd-103">Evitar saturaciones del búfer</span><span class="sxs-lookup"><span data-stu-id="452cd-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="452cd-104">Una saturación del búfer es uno de los orígenes más comunes de riesgos para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="452cd-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="452cd-105">Una saturación del búfer se produce esencialmente al tratar la entrada externa no comprobada como datos de confianza.</span><span class="sxs-lookup"><span data-stu-id="452cd-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="452cd-106">La acción de copiar estos datos, mediante operaciones como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy**, puede crear resultados inesperados, lo que permite daños en el sistema.</span><span class="sxs-lookup"><span data-stu-id="452cd-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="452cd-107">En el mejor de los casos, la aplicación se anulará con un volcado de memoria principal, un error de segmentación o una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="452cd-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="452cd-108">En el peor de los casos, un atacante puede aprovechar la saturación del búfer introduciendo y ejecutando otro código malintencionado en el proceso.</span><span class="sxs-lookup"><span data-stu-id="452cd-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="452cd-109">La copia de los datos no comprobados en un búfer basado en la pila es la causa más común de los errores explotables.</span><span class="sxs-lookup"><span data-stu-id="452cd-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="452cd-110">Las saturaciones del búfer pueden producirse de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="452cd-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="452cd-111">En la lista siguiente se proporciona una breve introducción a algunos tipos de situaciones de saturación del búfer y se ofrecen algunas ideas y recursos para ayudarle a evitar la creación de nuevos riesgos y a mitigar los existentes:</span><span class="sxs-lookup"><span data-stu-id="452cd-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="452cd-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Saturaciones estáticas del búfer</span><span class="sxs-lookup"><span data-stu-id="452cd-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="452cd-113">Una saturación del búfer estático se produce cuando un búfer, que se ha declarado en la pila, se escribe en con más datos de los que se asignaron para contener.</span><span class="sxs-lookup"><span data-stu-id="452cd-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="452cd-114">Las versiones menos aparente de este error se producen cuando los datos de entrada del usuario no comprobados se copian directamente en una variable estática, lo que produce daños en la pila.</span><span class="sxs-lookup"><span data-stu-id="452cd-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="452cd-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Saturaciones del montón</span><span class="sxs-lookup"><span data-stu-id="452cd-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="452cd-116">Las saturaciones del montón, como las saturaciones del búfer estático, pueden provocar daños en la memoria y la pila.</span><span class="sxs-lookup"><span data-stu-id="452cd-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="452cd-117">Dado que las saturaciones del montón se producen en la memoria del montón en lugar de en la pila, algunas personas consideran que son menos capaces de provocar problemas graves. No obstante, las saturaciones del montón requieren un cuidado de programación real y son como capaces de permitir riesgos del sistema como saturaciones del búfer estático.</span><span class="sxs-lookup"><span data-stu-id="452cd-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="452cd-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errores de indización de matriz</span><span class="sxs-lookup"><span data-stu-id="452cd-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="452cd-119">Los errores de indización de matriz también son un origen de saturaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="452cd-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="452cd-120">La comprobación de los límites cuidadosos y la administración de índices ayudarán a evitar este tipo de saturación de la memoria.</span><span class="sxs-lookup"><span data-stu-id="452cd-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="452cd-121">Evitar las saturaciones del búfer consiste principalmente en escribir código correcto.</span><span class="sxs-lookup"><span data-stu-id="452cd-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="452cd-122">Valide siempre todas las entradas y genere un error correctamente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="452cd-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="452cd-123">Para obtener más información sobre cómo escribir código seguro, vea los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="452cd-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="452cd-124">Maguire, Steve \[ 1993 \] , *escritura de código sólido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="452cd-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="452cd-125">Howard, Michael y LeBlanc, David \[ 2003 \] , *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="452cd-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="452cd-126">Es posible que estos recursos no estén disponibles en algunos idiomas y países.</span><span class="sxs-lookup"><span data-stu-id="452cd-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="452cd-127">El control de cadenas seguras es un problema de larga duración que se sigue solucionando siguiendo los buenos procedimientos de programación y con frecuencia mediante el uso de y el reajuste de sistemas existentes con funciones seguras de control de cadenas.</span><span class="sxs-lookup"><span data-stu-id="452cd-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="452cd-128">Un ejemplo de este conjunto de funciones para el shell de Windows se inicia con [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="452cd-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 

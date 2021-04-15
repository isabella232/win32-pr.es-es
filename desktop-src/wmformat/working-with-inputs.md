---
title: Trabajar con entradas
description: Trabajar con entradas
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- SDK de Windows Media Format, trabajar con entradas
- Advanced Systems Format (ASF), trabajar con entradas
- ASF (formato de sistemas avanzados), trabajar con entradas
- perfiles, trabajar con entradas
- flujos, trabajar con entradas
- códecs, trabajar con entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486719"
---
# <a name="working-with-inputs"></a><span data-ttu-id="842ff-109">Trabajar con entradas</span><span class="sxs-lookup"><span data-stu-id="842ff-109">Working with Inputs</span></span>

<span data-ttu-id="842ff-110">Del mismo modo que la configuración de la secuencia adecuada en el perfil es necesaria para que el códec pueda comprimir un flujo, también debe asegurarse de que el tipo de medio sin comprimir que se pasa al escritor se describe con precisión.</span><span class="sxs-lookup"><span data-stu-id="842ff-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="842ff-111">Cada códec de Windows Media tiene asociado un tipo de entrada predeterminado, pero se admiten varios tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="842ff-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="842ff-112">Puede examinar las entradas admitidas y seleccionar la que coincida con los datos.</span><span class="sxs-lookup"><span data-stu-id="842ff-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="842ff-113">El proceso de trabajo con entradas se resume en los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="842ff-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="842ff-114">Cuando se carga un perfil para que lo use el escritor, el objeto de escritor asigna un número de entrada para cada conexión del perfil.</span><span class="sxs-lookup"><span data-stu-id="842ff-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="842ff-115">Para obtener más información acerca de la carga de perfiles para el escritor, consulte [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="842ff-116">A menos que use la exclusión mutua por velocidad de bits, existe una conexión para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="842ff-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="842ff-117">Las secuencias que se excluyen mutuamente con la velocidad de bits comparten una única conexión.</span><span class="sxs-lookup"><span data-stu-id="842ff-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="842ff-118">La aplicación debe identificar los números de entrada del archivo.</span><span class="sxs-lookup"><span data-stu-id="842ff-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="842ff-119">Para obtener más información acerca de la identificación de números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="842ff-120">Para cada entrada, debe asegurarse de que el formato de entrada coincide con los datos.</span><span class="sxs-lookup"><span data-stu-id="842ff-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="842ff-121">Puede enumerar los formatos de entrada admitidos por el SDK.</span><span class="sxs-lookup"><span data-stu-id="842ff-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="842ff-122">Para obtener más información, vea [para enumerar los formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="842ff-123">No se pueden enumerar los formatos de entrada de secuencias o flujos arbitrarios que ya están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="842ff-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="842ff-124">Para obtener más información sobre estos casos especiales, consulte [entradas de secuencias arbitrarias y precomprimidas](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="842ff-125">Asigne el formato de entrada correcto para cada conexión.</span><span class="sxs-lookup"><span data-stu-id="842ff-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="842ff-126">Para obtener más información, vea [asignar formatos de entrada](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="842ff-127">Algunas características de los códecs y del escritor se configuran en el momento de la codificación en lugar de en el perfil.</span><span class="sxs-lookup"><span data-stu-id="842ff-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="842ff-128">Para configurar estas características, debe usar la configuración de entrada.</span><span class="sxs-lookup"><span data-stu-id="842ff-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="842ff-129">Para obtener más información, vea [para establecer la configuración de entrada](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="842ff-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="842ff-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="842ff-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="842ff-131">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="842ff-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





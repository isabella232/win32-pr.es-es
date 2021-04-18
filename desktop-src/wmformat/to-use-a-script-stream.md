---
title: Para usar una secuencia de script
description: Para usar una secuencia de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- secuencias de scripts, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357742"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="992ed-107">Para usar una secuencia de script</span><span class="sxs-lookup"><span data-stu-id="992ed-107">To Use a Script Stream</span></span>

<span data-ttu-id="992ed-108">En esta sección se describe cómo enviar datos de script al escritor para incluirlos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="992ed-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="992ed-109">Para obtener información sobre cómo incluir secuencias de scripts en perfiles, vea [configuración de tipos de secuencia arbitrarios](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="992ed-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="992ed-110">Cada script consta de dos cadenas: una cadena de *tipo* y una cadena de *argumento* .</span><span class="sxs-lookup"><span data-stu-id="992ed-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="992ed-111">Se debe dar formato a los datos del script antes de que se envíen al escritor.</span><span class="sxs-lookup"><span data-stu-id="992ed-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="992ed-112">Las cadenas se deben concatenar, separarse mediante un carácter **nulo** y terminar con un carácter **nulo** .</span><span class="sxs-lookup"><span data-stu-id="992ed-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="992ed-113">En el ejemplo siguiente se muestra un script legítimo:</span><span class="sxs-lookup"><span data-stu-id="992ed-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="992ed-114">U</span><span class="sxs-lookup"><span data-stu-id="992ed-114">U</span></span>   | <span data-ttu-id="992ed-115">R</span><span class="sxs-lookup"><span data-stu-id="992ed-115">R</span></span>   | <span data-ttu-id="992ed-116">L</span><span class="sxs-lookup"><span data-stu-id="992ed-116">L</span></span>   | <span data-ttu-id="992ed-117">\\0</span><span class="sxs-lookup"><span data-stu-id="992ed-117">\\0</span></span> | <span data-ttu-id="992ed-118">h</span><span class="sxs-lookup"><span data-stu-id="992ed-118">h</span></span>   | <span data-ttu-id="992ed-119">t</span><span class="sxs-lookup"><span data-stu-id="992ed-119">t</span></span>   | <span data-ttu-id="992ed-120">t</span><span class="sxs-lookup"><span data-stu-id="992ed-120">t</span></span>   | <span data-ttu-id="992ed-121">p</span><span class="sxs-lookup"><span data-stu-id="992ed-121">p</span></span>   | <span data-ttu-id="992ed-122">:</span><span class="sxs-lookup"><span data-stu-id="992ed-122">:</span></span>   | /   | /   | <span data-ttu-id="992ed-123">w</span><span class="sxs-lookup"><span data-stu-id="992ed-123">w</span></span>   | <span data-ttu-id="992ed-124">w</span><span class="sxs-lookup"><span data-stu-id="992ed-124">w</span></span>   | <span data-ttu-id="992ed-125">w</span><span class="sxs-lookup"><span data-stu-id="992ed-125">w</span></span>   | <span data-ttu-id="992ed-126">.</span><span class="sxs-lookup"><span data-stu-id="992ed-126">.</span></span>   | <span data-ttu-id="992ed-127">a</span><span class="sxs-lookup"><span data-stu-id="992ed-127">a</span></span>   | <span data-ttu-id="992ed-128">d</span><span class="sxs-lookup"><span data-stu-id="992ed-128">d</span></span>   | <span data-ttu-id="992ed-129">a</span><span class="sxs-lookup"><span data-stu-id="992ed-129">a</span></span>   | <span data-ttu-id="992ed-130">t</span><span class="sxs-lookup"><span data-stu-id="992ed-130">t</span></span>   | <span data-ttu-id="992ed-131">u</span><span class="sxs-lookup"><span data-stu-id="992ed-131">u</span></span>   | <span data-ttu-id="992ed-132">m</span><span class="sxs-lookup"><span data-stu-id="992ed-132">m</span></span>   | <span data-ttu-id="992ed-133">.</span><span class="sxs-lookup"><span data-stu-id="992ed-133">.</span></span>   | <span data-ttu-id="992ed-134">c</span><span class="sxs-lookup"><span data-stu-id="992ed-134">c</span></span>   | <span data-ttu-id="992ed-135">o</span><span class="sxs-lookup"><span data-stu-id="992ed-135">o</span></span>   | <span data-ttu-id="992ed-136">m</span><span class="sxs-lookup"><span data-stu-id="992ed-136">m</span></span>   | <span data-ttu-id="992ed-137">\\0</span><span class="sxs-lookup"><span data-stu-id="992ed-137">\\0</span></span> |



 

<span data-ttu-id="992ed-138">Cada par de comandos de script debe escribirse como un ejemplo en el escritor.</span><span class="sxs-lookup"><span data-stu-id="992ed-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="992ed-139">Para obtener más información sobre cómo escribir ejemplos, consulte [para escribir ejemplos](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="992ed-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="992ed-140">Cuando se reproduzca el archivo ASF, el lector (o lector sincrónico) entregará los comandos de script en el orden temporal de la presentación.</span><span class="sxs-lookup"><span data-stu-id="992ed-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="992ed-141">Es responsabilidad de la aplicación analizar las dos cadenas y responder al comando de script.</span><span class="sxs-lookup"><span data-stu-id="992ed-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="992ed-142">Al usar DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.</span><span class="sxs-lookup"><span data-stu-id="992ed-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="992ed-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="992ed-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="992ed-144">**Usar comandos de script**</span><span class="sxs-lookup"><span data-stu-id="992ed-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





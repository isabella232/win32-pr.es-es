---
title: Para usar una secuencia de scripts
description: Para usar una secuencia de scripts
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK,secuencias de script
- Formato de sistemas avanzados (ASF), secuencias de script
- ASF (formato de sistemas avanzados), secuencias de script
- secuencias de script, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444736"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="c0420-107">Para usar una secuencia de scripts</span><span class="sxs-lookup"><span data-stu-id="c0420-107">To Use a Script Stream</span></span>

<span data-ttu-id="c0420-108">En esta sección se describe cómo enviar datos de script al escritor para su inclusión en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c0420-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="c0420-109">Para obtener información sobre cómo incluir secuencias de script en perfiles, vea [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="c0420-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="c0420-110">Cada script consta de dos cadenas, una *cadena de tipo* y una cadena de *argumento.*</span><span class="sxs-lookup"><span data-stu-id="c0420-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="c0420-111">Los datos del script deben tener formato antes de enviarse al escritor.</span><span class="sxs-lookup"><span data-stu-id="c0420-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="c0420-112">Las cadenas se deben concatenar, separar por un **carácter NULL** y terminar con un **carácter** NULL.</span><span class="sxs-lookup"><span data-stu-id="c0420-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="c0420-113">En el ejemplo siguiente se muestra un script legítimo:</span><span class="sxs-lookup"><span data-stu-id="c0420-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="c0420-114">U</span><span class="sxs-lookup"><span data-stu-id="c0420-114">U</span></span>   | <span data-ttu-id="c0420-115">R</span><span class="sxs-lookup"><span data-stu-id="c0420-115">R</span></span>   | <span data-ttu-id="c0420-116">L</span><span class="sxs-lookup"><span data-stu-id="c0420-116">L</span></span>   | &nbsp; | <span data-ttu-id="c0420-117">h</span><span class="sxs-lookup"><span data-stu-id="c0420-117">h</span></span>   | <span data-ttu-id="c0420-118">t</span><span class="sxs-lookup"><span data-stu-id="c0420-118">t</span></span>   | <span data-ttu-id="c0420-119">t</span><span class="sxs-lookup"><span data-stu-id="c0420-119">t</span></span>   | <span data-ttu-id="c0420-120">p</span><span class="sxs-lookup"><span data-stu-id="c0420-120">p</span></span>   | <span data-ttu-id="c0420-121">:</span><span class="sxs-lookup"><span data-stu-id="c0420-121">:</span></span>   | /   | /   | <span data-ttu-id="c0420-122">w</span><span class="sxs-lookup"><span data-stu-id="c0420-122">w</span></span>   | <span data-ttu-id="c0420-123">w</span><span class="sxs-lookup"><span data-stu-id="c0420-123">w</span></span>   | <span data-ttu-id="c0420-124">w</span><span class="sxs-lookup"><span data-stu-id="c0420-124">w</span></span>   | <span data-ttu-id="c0420-125">.</span><span class="sxs-lookup"><span data-stu-id="c0420-125">.</span></span>   | <span data-ttu-id="c0420-126">a</span><span class="sxs-lookup"><span data-stu-id="c0420-126">a</span></span>   | <span data-ttu-id="c0420-127">d</span><span class="sxs-lookup"><span data-stu-id="c0420-127">d</span></span>   | <span data-ttu-id="c0420-128">a</span><span class="sxs-lookup"><span data-stu-id="c0420-128">a</span></span>   | <span data-ttu-id="c0420-129">t</span><span class="sxs-lookup"><span data-stu-id="c0420-129">t</span></span>   | <span data-ttu-id="c0420-130">u</span><span class="sxs-lookup"><span data-stu-id="c0420-130">u</span></span>   | <span data-ttu-id="c0420-131">m</span><span class="sxs-lookup"><span data-stu-id="c0420-131">m</span></span>   | <span data-ttu-id="c0420-132">.</span><span class="sxs-lookup"><span data-stu-id="c0420-132">.</span></span>   | <span data-ttu-id="c0420-133">c</span><span class="sxs-lookup"><span data-stu-id="c0420-133">c</span></span>   | <span data-ttu-id="c0420-134">o</span><span class="sxs-lookup"><span data-stu-id="c0420-134">o</span></span>   | <span data-ttu-id="c0420-135">m</span><span class="sxs-lookup"><span data-stu-id="c0420-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="c0420-136">Cada par de comandos de script debe escribirse como un ejemplo para el escritor.</span><span class="sxs-lookup"><span data-stu-id="c0420-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="c0420-137">Para obtener más información sobre cómo escribir ejemplos, vea [Para escribir ejemplos.](to-write-samples.md)</span><span class="sxs-lookup"><span data-stu-id="c0420-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="c0420-138">Cuando se reproduce el archivo ASF, el lector (o lector sincrónico) entregará los comandos de script en el orden de tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="c0420-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="c0420-139">Es responsabilidad de la aplicación analizar las dos cadenas y responder al comando de script.</span><span class="sxs-lookup"><span data-stu-id="c0420-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="c0420-140">Cuando se usa DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.</span><span class="sxs-lookup"><span data-stu-id="c0420-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c0420-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0420-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0420-142">**Uso de comandos de script**</span><span class="sxs-lookup"><span data-stu-id="c0420-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





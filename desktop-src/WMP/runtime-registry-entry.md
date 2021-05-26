---
title: Entrada del Registro en tiempo de ejecución
description: Entrada del Registro en tiempo de ejecución
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Reproductor de Windows Media,entradas del Registro en tiempo de ejecución
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,registry
- registry,file name extensions
- registro, entradas en tiempo de ejecución
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- entradas del Registro en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424114"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="01178-111">Entrada del Registro en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="01178-111">Runtime Registry Entry</span></span>

<span data-ttu-id="01178-112">Cuando Reproductor de Windows Media encuentra una extensión de nombre de archivo personalizada, busca una subclave del Registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="01178-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="01178-113">La subclave se describe en [File Name Extension Registry Settings (Configuración del Registro de extensiones de nombre de archivo).](file-name-extension-registry-settings.md)</span><span class="sxs-lookup"><span data-stu-id="01178-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="01178-114">Una de las entradas del Registro que pueden aparecer en la subclave de la extensión es la entrada **runtime.**</span><span class="sxs-lookup"><span data-stu-id="01178-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="01178-115">La **entrada Runtime** especifica la tecnología subyacente que Reproductor de Windows Media puede usar para reproducir o convertir archivos multimedia digitales que tienen la extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="01178-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="01178-116">La **entrada Runtime** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="01178-116">The **Runtime** entry has the following form.</span></span>



|   <span data-ttu-id="01178-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="01178-117">Name</span></span>   |   <span data-ttu-id="01178-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="01178-118">Type</span></span>         |   <span data-ttu-id="01178-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01178-119">Value</span></span>                                                       |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="01178-120">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="01178-120">Runtime</span></span>  | <span data-ttu-id="01178-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="01178-121">**REG\_DWORD**</span></span> | <span data-ttu-id="01178-122">Entero positivo que identifica la tecnología subyacente.</span><span class="sxs-lookup"><span data-stu-id="01178-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="01178-123">El valor de la entrada **runtime** debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="01178-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="01178-124">**Valor (decimal)**</span><span class="sxs-lookup"><span data-stu-id="01178-124">**Value (decimal)**</span></span> | <span data-ttu-id="01178-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01178-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="01178-126">6</span><span class="sxs-lookup"><span data-stu-id="01178-126">6</span></span>                   | <span data-ttu-id="01178-127">Representar mediante el SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="01178-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="01178-128">7</span><span class="sxs-lookup"><span data-stu-id="01178-128">7</span></span>                   | <span data-ttu-id="01178-129">Representar mediante Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01178-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="01178-130">13</span><span class="sxs-lookup"><span data-stu-id="01178-130">13</span></span>                  | <span data-ttu-id="01178-131">Convierta el archivo mediante el complemento de conversión especificado.</span><span class="sxs-lookup"><span data-stu-id="01178-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="01178-132">Requiere Reproductor de Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="01178-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="01178-133">Los **valores de** entrada del Registro en tiempo de ejecución 6 y 7 son compatibles con Reproductor de Windows Media serie 9 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="01178-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="01178-134">El valor 13 es compatible con Reproductor de Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="01178-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01178-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01178-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01178-136">**Subclave ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="01178-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="01178-137">**Configuración del Registro de extensiones de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="01178-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





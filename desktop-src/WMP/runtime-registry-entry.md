---
title: Entrada del registro en tiempo de ejecución
description: Entrada del registro en tiempo de ejecución
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, entradas del registro en tiempo de ejecución
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas en tiempo de ejecución
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- entradas del registro en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075967"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="d8fff-111">Entrada del registro en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d8fff-111">Runtime Registry Entry</span></span>

<span data-ttu-id="d8fff-112">Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión.</span><span class="sxs-lookup"><span data-stu-id="d8fff-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="d8fff-113">La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d8fff-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="d8fff-114">Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada **en tiempo de ejecución** .</span><span class="sxs-lookup"><span data-stu-id="d8fff-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="d8fff-115">La entrada **en tiempo de ejecución** especifica la tecnología subyacente que Windows Media Player puede usar para reproducir o convertir archivos multimedia digitales que tienen la extensión personalizada.</span><span class="sxs-lookup"><span data-stu-id="d8fff-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="d8fff-116">La entrada **en tiempo de ejecución** tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="d8fff-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="d8fff-117">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d8fff-117">**Name**</span></span> | <span data-ttu-id="d8fff-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8fff-118">**Type**</span></span>       | <span data-ttu-id="d8fff-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d8fff-119">**Value**</span></span>                                                     |
| <span data-ttu-id="d8fff-120">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d8fff-120">Runtime</span></span>  | <span data-ttu-id="d8fff-121">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="d8fff-121">**REG\_DWORD**</span></span> | <span data-ttu-id="d8fff-122">Un entero positivo que identifica la tecnología subyacente.</span><span class="sxs-lookup"><span data-stu-id="d8fff-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="d8fff-123">El valor de la entrada **en tiempo de ejecución** debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8fff-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="d8fff-124">**Valor (decimal)**</span><span class="sxs-lookup"><span data-stu-id="d8fff-124">**Value (decimal)**</span></span> | <span data-ttu-id="d8fff-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8fff-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fff-126">6</span><span class="sxs-lookup"><span data-stu-id="d8fff-126">6</span></span>                   | <span data-ttu-id="d8fff-127">Se representa mediante el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d8fff-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="d8fff-128">7</span><span class="sxs-lookup"><span data-stu-id="d8fff-128">7</span></span>                   | <span data-ttu-id="d8fff-129">Se representa mediante Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d8fff-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="d8fff-130">13</span><span class="sxs-lookup"><span data-stu-id="d8fff-130">13</span></span>                  | <span data-ttu-id="d8fff-131">Convierte el archivo mediante el complemento de conversión especificado.</span><span class="sxs-lookup"><span data-stu-id="d8fff-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="d8fff-132">Requiere Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d8fff-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="d8fff-133">Los valores 6 y 7 de la entrada del registro **en tiempo de ejecución** son compatibles con Windows Media Player 9 series y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d8fff-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="d8fff-134">El valor 13 es compatible con Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d8fff-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8fff-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8fff-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8fff-136">**Subclave ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="d8fff-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="d8fff-137">**Configuración del registro de la extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="d8fff-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





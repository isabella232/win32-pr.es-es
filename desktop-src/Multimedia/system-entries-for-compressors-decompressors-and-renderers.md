---
title: Entradas del sistema para compresores, descompresores y representadores
description: Entradas del sistema para compresores, descompresores y representadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Vídeo para Windows (VFW), entradas del sistema compresores
- VFW (vídeo para Windows), entradas del sistema compresores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778835"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="95dd3-105">Entradas del sistema para compresores, descompresores y representadores</span><span class="sxs-lookup"><span data-stu-id="95dd3-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="95dd3-106">El sistema utiliza las entradas del registro para buscar los controladores VCM.</span><span class="sxs-lookup"><span data-stu-id="95dd3-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="95dd3-107">Estas entradas tienen el formato de códigos de 2 4 caracteres separados por un punto.</span><span class="sxs-lookup"><span data-stu-id="95dd3-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="95dd3-108">El sistema define el primer código de cuatro caracteres y puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="95dd3-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="95dd3-109">Código de cuatro caracteres</span><span class="sxs-lookup"><span data-stu-id="95dd3-109">Four-character code</span></span> | <span data-ttu-id="95dd3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="95dd3-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="95dd3-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="95dd3-111">"VIDC"</span></span>              | <span data-ttu-id="95dd3-112">Identifica los compresores y descompresores.</span><span class="sxs-lookup"><span data-stu-id="95dd3-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="95dd3-113">VID</span><span class="sxs-lookup"><span data-stu-id="95dd3-113">"VIDS"</span></span>              | <span data-ttu-id="95dd3-114">Identifica los representadores de flujos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="95dd3-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="95dd3-115">"TXTS"</span><span class="sxs-lookup"><span data-stu-id="95dd3-115">"TXTS"</span></span>              | <span data-ttu-id="95dd3-116">Identifica los representadores de flujo de texto.</span><span class="sxs-lookup"><span data-stu-id="95dd3-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="95dd3-117">"AUDS"</span><span class="sxs-lookup"><span data-stu-id="95dd3-117">"AUDS"</span></span>              | <span data-ttu-id="95dd3-118">Identifica los controladores de secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="95dd3-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="95dd3-119">Los representadores personalizados pueden definir sus propios códigos de cuatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="95dd3-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="95dd3-120">El controlador define el segundo código de cuatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="95dd3-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="95dd3-121">Normalmente, el segundo código de cuatro caracteres corresponde al tipo de datos que el controlador puede controlar.</span><span class="sxs-lookup"><span data-stu-id="95dd3-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="95dd3-122">Al abrir un controlador VCM, una aplicación especifica el tipo de controlador y el tipo de controlador de datos que necesita.</span><span class="sxs-lookup"><span data-stu-id="95dd3-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="95dd3-123">Normalmente, esta información procede del encabezado de flujo.</span><span class="sxs-lookup"><span data-stu-id="95dd3-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="95dd3-124">El sistema intenta abrir el controlador de datos especificado, pero si se produce un error, el sistema busca en el registro un controlador que tenga el controlador necesario.</span><span class="sxs-lookup"><span data-stu-id="95dd3-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="95dd3-125">Al buscar el controlador, el sistema intenta coincidir con los códigos de cuatro caracteres especificados para el tipo de controlador y el controlador de datos con los especificados en la entrada del controlador.</span><span class="sxs-lookup"><span data-stu-id="95dd3-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="95dd3-126">Por ejemplo, si una aplicación especifica el compresor MSSQ, el sistema busca en el registro la entrada del controlador VIDC. MSSQ.</span><span class="sxs-lookup"><span data-stu-id="95dd3-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="95dd3-127">Si no encuentra ninguna coincidencia, abre cada controlador correspondiente al tipo de controlador y localiza una que puede controlar el tipo de datos que la aplicación especifica.</span><span class="sxs-lookup"><span data-stu-id="95dd3-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="95dd3-128">En el ejemplo anterior, si el sistema no encontró VIDC. MSSQ, abriría todos los controladores con el código de cuatro caracteres "VIDC" y buscaría uno que pueda controlar los datos.</span><span class="sxs-lookup"><span data-stu-id="95dd3-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 





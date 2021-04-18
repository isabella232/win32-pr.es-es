---
title: Configuración de tipos de flujo arbitrarios
description: Configuración de tipos de flujo arbitrarios
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flujos, configurar tipos de secuencia arbitrarios
- códecs, configurar tipos de secuencias arbitrarios
- flujos, GenProfile
- códecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714173"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="fa4fa-108">Configuración de tipos de flujo arbitrarios</span><span class="sxs-lookup"><span data-stu-id="fa4fa-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="fa4fa-109">La mayoría de los tipos de secuencias arbitrarias solo necesitan una velocidad de bits, una ventana de búfer y un tipo de medio principal adecuado en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="fa4fa-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="fa4fa-110">Sin embargo, algunos tipos arbitrarios requieren una configuración adicional.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="fa4fa-111">Si tiene problemas para configurar una secuencia, consulte la aplicación de ejemplo llamada GenProfile, que se incluye con este SDK.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="fa4fa-112">La biblioteca definida en GenProfile contiene código para incluir todos los tipos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="fa4fa-113">Para obtener más información sobre GenProfile y los otros ejemplos, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="fa4fa-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="fa4fa-114">En las secciones siguientes se describe cómo configurar tipos de secuencia arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="fa4fa-115">Sección</span><span class="sxs-lookup"><span data-stu-id="fa4fa-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="fa4fa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa4fa-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa4fa-117">Configurar secuencias de scripts</span><span class="sxs-lookup"><span data-stu-id="fa4fa-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="fa4fa-118">Describe cómo configurar secuencias de scripts.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="fa4fa-119">Configuración de secuencias de transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="fa4fa-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="fa4fa-120">Describe cómo configurar secuencias de transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="fa4fa-121">Configuración de secuencias Web</span><span class="sxs-lookup"><span data-stu-id="fa4fa-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="fa4fa-122">Describe cómo configurar secuencias Web.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="fa4fa-123">Configurar secuencias de texto</span><span class="sxs-lookup"><span data-stu-id="fa4fa-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="fa4fa-124">Describe cómo configurar secuencias de texto.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="fa4fa-125">Configuración de secuencias arbitrarias personalizadas</span><span class="sxs-lookup"><span data-stu-id="fa4fa-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="fa4fa-126">Describe cómo configurar secuencias para tipos de secuencia arbitrarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="fa4fa-127">Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios</span><span class="sxs-lookup"><span data-stu-id="fa4fa-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="fa4fa-128">Describe cómo calcular la velocidad de bits y la configuración de la ventana de búfer para una secuencia arbitraria.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fa4fa-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa4fa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa4fa-130">**Flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="fa4fa-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="fa4fa-131">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="fa4fa-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 





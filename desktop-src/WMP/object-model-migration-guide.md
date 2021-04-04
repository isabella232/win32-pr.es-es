---
title: Guía de migración del modelo de objetos
description: Guía de migración del modelo de objetos
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Media Player de Windows, modelo de objetos
- Windows Media Player, guía de migración
- Modelo de objetos de Windows Media Player, guía de migración
- modelo de objetos, guía de migración
- Control ActiveX de Windows Media Player, guía de migración
- Control ActiveX, guía de migración
- Control ActiveX móvil de Windows Media Player, guía de migración
- Windows Media Player Mobile, modelo de objetos
- Windows Media Player Mobile, guía de migración
- Guía de migración, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076150"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="966b9-113">Guía de migración del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="966b9-113">Object Model Migration Guide</span></span>

<span data-ttu-id="966b9-114">Windows Media Player 7 presentó un nuevo modelo de objetos que ofrece un nuevo conjunto de funcionalidades que puede usar para mejorar sus páginas Web.</span><span class="sxs-lookup"><span data-stu-id="966b9-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="966b9-115">Las versiones posteriores han ampliado el modelo de objetos de la versión 7 con propiedades, métodos y eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="966b9-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="966b9-116">Sin embargo, el nuevo modelo de objetos difiere sustancialmente del modelo de objetos de Windows Media Player 6,4, por lo que debe saber cómo actualizar el código existente si desea admitir Windows Media Player 7 y versiones posteriores en sus proyectos.</span><span class="sxs-lookup"><span data-stu-id="966b9-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="966b9-117">Para obtener un ejemplo que muestra cómo detectar la versión de Windows Media Player del usuario y el explorador actual, consulte el ejemplo denominado "detección" que se instala con este SDK.</span><span class="sxs-lookup"><span data-stu-id="966b9-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="966b9-118">Para obtener más información acerca de los ejemplos, vea [ejemplos](samples.md).</span><span class="sxs-lookup"><span data-stu-id="966b9-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="966b9-119">En esta guía se hace referencia al nuevo modelo de objetos de como el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="966b9-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="966b9-120">Para obtener información detallada sobre qué funcionalidad está disponible en cada versión de Windows Media Player, consulte [Referencia del modelo de objetos para scripting](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="966b9-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="966b9-121">Estos problemas del modelo de objetos se tratan en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="966b9-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="966b9-122">Diferencias entre los modelos de objetos</span><span class="sxs-lookup"><span data-stu-id="966b9-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="966b9-123">Usar el modelo de objetos de Windows Media Player 7 o posterior</span><span class="sxs-lookup"><span data-stu-id="966b9-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="966b9-124">Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="966b9-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="966b9-125">Reproducción</span><span class="sxs-lookup"><span data-stu-id="966b9-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="966b9-126">Subtítulos (CC)</span><span class="sxs-lookup"><span data-stu-id="966b9-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="966b9-127">DISCOS</span><span class="sxs-lookup"><span data-stu-id="966b9-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="966b9-128">Comparación detallada del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="966b9-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="966b9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="966b9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="966b9-130">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="966b9-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 





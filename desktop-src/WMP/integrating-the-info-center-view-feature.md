---
title: Integración de la característica de vista de centro de información
description: Integración de la característica de vista de centro de información
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player tiendas en línea, integración de la vista del centro de información
- tiendas en línea, integración de la vista del centro de información
- Escriba 1 tiendas en línea, integrando la vista del centro de información
- Escriba 2 tiendas en línea, integrando la vista del centro de información
- Windows Media Player tiendas en línea, vista del centro de información
- tiendas en línea, vista del centro de información
- tipo 1 tiendas en línea, vista del centro de información
- tipo 2 tiendas en línea, vista del centro de información
- integración de la vista del centro de información
- Vista del centro de información
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685610"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="821a7-113">Integración de la característica de vista de centro de información</span><span class="sxs-lookup"><span data-stu-id="821a7-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="821a7-114">Windows Media Player permite a los usuarios abrir y cerrar la característica de vista de centro de información.</span><span class="sxs-lookup"><span data-stu-id="821a7-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="821a7-115">Info Center View es la característica en la que los usuarios esperan encontrar información enriquecida y ampliada sobre contenido multimedia digital específico.</span><span class="sxs-lookup"><span data-stu-id="821a7-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="821a7-116">Cuando el usuario elige abrir info Center View, Windows Media Player llama a en la tienda de música actual para mostrar la Página Web de la vista de info Center especificada por el atributo **URL** del elemento **Infocenter** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="821a7-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="821a7-117">Para recuperar información sobre el contenido multimedia digital que se está reproduciendo actualmente, debe incrustar una instancia del control de Windows Media Player en la página web y utilizar el modelo de objetos del reproductor.</span><span class="sxs-lookup"><span data-stu-id="821a7-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="821a7-118">Por ejemplo, para recuperar el título, puede usar el siguiente código JScript:</span><span class="sxs-lookup"><span data-stu-id="821a7-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="821a7-119">Directrices para la vista del centro de información</span><span class="sxs-lookup"><span data-stu-id="821a7-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="821a7-120">Al crear la Página Web de la **vista de centro de información** , use las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="821a7-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="821a7-121">La página debe identificar claramente la tienda en línea que proporciona la información.</span><span class="sxs-lookup"><span data-stu-id="821a7-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="821a7-122">Para ello, puede mostrar el logotipo de forma destacada, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="821a7-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="821a7-123">La página debe incluir un vínculo a la declaración de privacidad de la empresa.</span><span class="sxs-lookup"><span data-stu-id="821a7-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="821a7-124">Evite la navegación de página dentro de la característica de vista de centro de información siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="821a7-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="821a7-125">Debe navegar a la tienda en línea para la mayoría de las actividades.</span><span class="sxs-lookup"><span data-stu-id="821a7-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="821a7-126">Es mejor proporcionar información valiosa sin necesidad de que el usuario instale programas o inicie sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="821a7-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="821a7-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="821a7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821a7-128">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="821a7-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="821a7-129">**Elemento InfoCenter**</span><span class="sxs-lookup"><span data-stu-id="821a7-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="821a7-130">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="821a7-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="821a7-131">**Usar el control Media Player de Windows en una página web**</span><span class="sxs-lookup"><span data-stu-id="821a7-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





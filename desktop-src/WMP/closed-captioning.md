---
title: Subtítulos (CC)
description: Subtítulos (CC)
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player, migrar subtítulos (CC)
- Modelo de objetos de Windows Media Player, subtítulos (CC) Smigrating
- modelo de objetos, migrar subtítulos
- Windows Media Player Mobile, migrar subtítulos (CC)
- Control ActiveX de Windows Media Player, migrar subtítulos (CC)
- Control ActiveX móvil de Windows Media Player, migración de subtítulos cerrados
- Control ActiveX, migrar subtítulos (CC)
- Intercambio de multimedia accesible sincronizado (SAMI), migración de subtítulos cerrados
- SAMI (intercambio de multimedia accesible sincronizado), migración de subtítulos cerrados
- Guía de migración, intercambio de multimedia accesible sincronizado (SAMI)
- Guía de migración, subtítulos (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149106"
---
# <a name="closed-captioning"></a><span data-ttu-id="96c68-121">Subtítulos (CC)</span><span class="sxs-lookup"><span data-stu-id="96c68-121">Closed Captioning</span></span>

<span data-ttu-id="96c68-122">El control ActiveX de Windows Media Player 6,4 incluye un panel de presentación de un título cerrado integrado que, cuando se hace visible, habilita los subtítulos (SAMI) de intercambio de medios accesibles sincronizados y muestra el texto de la leyenda cerrada.</span><span class="sxs-lookup"><span data-stu-id="96c68-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="96c68-123">El control Windows Media Player 7 o posterior habilita la presentación de la leyenda cerrada de SAMI mediante un **<DIV>** elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="96c68-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="96c68-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="96c68-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="96c68-125">Esta técnica proporciona una flexibilidad completa, ya que puede diseñar su página web para mostrar los subtítulos (CC) de una manera personalizada. ya no es necesario que la presentación de subtítulos cerrados esté en una ubicación fija adyacente a la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="96c68-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="96c68-126">Una vez que haya creado un área para mostrar los subtítulos cerrados, use *ClosedCaption*. propiedad **captioningID** para especificar la ubicación donde Windows Media Player representa el texto de la leyenda cerrada.</span><span class="sxs-lookup"><span data-stu-id="96c68-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="96c68-127">El kit de desarrollo de software (SDK) de Windows Media Player contiene un ejemplo funcional de un reproductor incrustado que muestra el texto de la leyenda cerrada.</span><span class="sxs-lookup"><span data-stu-id="96c68-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="96c68-128">Para obtener los ejemplos del SDK, descargue e instale el SDK de Windows Media Player completo en el sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96c68-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="96c68-129">Para obtener más información acerca de los subtítulos y SAMI, vea el [sitio web de accesibilidad de Microsoft](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="96c68-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96c68-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96c68-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96c68-131">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="96c68-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="96c68-132">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="96c68-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="96c68-133">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="96c68-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 





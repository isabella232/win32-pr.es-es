---
title: Usar el control Media Player de Windows en una página web
description: Usar el control Media Player de Windows en una página web
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- incrustación, páginas web
- Incrustación de páginas web, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269073"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="921c6-115">Usar el control Media Player de Windows en una página web</span><span class="sxs-lookup"><span data-stu-id="921c6-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="921c6-116">Incrustar el control de Media Player de Windows en una página web permite personalizar completamente el modo en que el usuario interactúa con el control.</span><span class="sxs-lookup"><span data-stu-id="921c6-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="921c6-117">Puede usar la interfaz proporcionada por el control o puede ocultarla y mostrar su propia interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="921c6-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="921c6-118">Puede especificar varias propiedades de control de Media Player de Windows en el punto en el que se incrusta el control, o puede establecer las propiedades del reproductor y llamar a los métodos del reproductor en el código de script.</span><span class="sxs-lookup"><span data-stu-id="921c6-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="921c6-119">En las secciones siguientes se describen los conceptos básicos de la incrustación del control en una página web.</span><span class="sxs-lookup"><span data-stu-id="921c6-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="921c6-120">Sección</span><span class="sxs-lookup"><span data-stu-id="921c6-120">Section</span></span>                                                                                                        | <span data-ttu-id="921c6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="921c6-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="921c6-122">Ocultar el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="921c6-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="921c6-123">Describe las opciones para ocultar el control Media Player de Windows cuando desea proporcionar su propia interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="921c6-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="921c6-124">Elementos PARAM de un elemento OBJECT</span><span class="sxs-lookup"><span data-stu-id="921c6-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="921c6-125">Describe cómo inicializar el control de Media Player de Windows al insertarlo.</span><span class="sxs-lookup"><span data-stu-id="921c6-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="921c6-126">Ejemplo sencillo de scripting en una página web</span><span class="sxs-lookup"><span data-stu-id="921c6-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="921c6-127">Describe un ejemplo simple, pero completo, de un control de reproductor incrustado con una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="921c6-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="921c6-128">Uso del control de Media Player de Windows con Firefox</span><span class="sxs-lookup"><span data-stu-id="921c6-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="921c6-129">Describe cómo insertar el control Media Player de Windows en una página web para que se muestre correctamente en un explorador Firefox.</span><span class="sxs-lookup"><span data-stu-id="921c6-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="921c6-130">Uso del Reproductor de Windows Media con Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="921c6-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="921c6-131">Describe cómo usar el control de Media Player de Windows con Netscape 7,1 y otros exploradores Web basados en Gecko.</span><span class="sxs-lookup"><span data-stu-id="921c6-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="921c6-132">El control Windows Media Player 10 Mobile contiene funcionalidad basada en un subconjunto de la funcionalidad proporcionada en la versión de escritorio del control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="921c6-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="921c6-133">Por lo tanto, se puede incrustar en una página web de Pocket Internet Explorer de la misma manera que el control de escritorio se incrusta en una página web de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="921c6-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="921c6-134">Para averiguar si un método, propiedad o evento determinado es compatible con el control móvil de Windows Media Player 10, vea [Referencia del modelo de objetos para scripting](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="921c6-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="921c6-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="921c6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="921c6-136">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="921c6-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 





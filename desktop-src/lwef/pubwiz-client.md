---
title: Diseño de Client-Side
description: El script en páginas HTML del lado servidor se comunica con el cliente del Asistente para orden de impresión en línea en el que se hospeda. Esta comunicación se logra a través de métodos y propiedades a los que tiene acceso el objeto Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- asistentes para publicación, diseño del lado cliente
- Window. external, asistentes para publicación
- asistentes para publicación, Window. external
- asistentes para la publicación, consideraciones de diseño
- asistentes para publicación, Asistente para impresión en línea
- Asistente para orden de impresión en línea, diseño del lado cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995231"
---
# <a name="client-side-design"></a><span data-ttu-id="ebf19-110">Diseño de Client-Side</span><span class="sxs-lookup"><span data-stu-id="ebf19-110">Client-Side Design</span></span>

<span data-ttu-id="ebf19-111">El script en páginas HTML del lado servidor se comunica con el cliente del Asistente para orden de impresión en línea en el que se hospeda.</span><span class="sxs-lookup"><span data-stu-id="ebf19-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="ebf19-112">Esta comunicación se logra a través de métodos y propiedades a los que tiene acceso el objeto **window. external** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="ebf19-113">Los temas siguientes se tratan en este documento.</span><span class="sxs-lookup"><span data-stu-id="ebf19-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="ebf19-114">Métodos y propiedades</span><span class="sxs-lookup"><span data-stu-id="ebf19-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="ebf19-115">Consideraciones de diseño</span><span class="sxs-lookup"><span data-stu-id="ebf19-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="ebf19-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebf19-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="ebf19-117">Métodos y propiedades</span><span class="sxs-lookup"><span data-stu-id="ebf19-117">Methods and Properties</span></span>

<span data-ttu-id="ebf19-118">Los siguientes métodos y propiedades están disponibles a través del objeto **window. external** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="ebf19-119">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="ebf19-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="ebf19-120">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="ebf19-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="ebf19-121">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="ebf19-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="ebf19-122">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="ebf19-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="ebf19-123">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="ebf19-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="ebf19-124">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="ebf19-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="ebf19-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebf19-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="ebf19-126">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="ebf19-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="ebf19-127">El script de la página del servidor llama a estos métodos para notificar al cliente los eventos durante el procedimiento de publicación.</span><span class="sxs-lookup"><span data-stu-id="ebf19-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="ebf19-128">Echemos un vistazo a [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) como ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebf19-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="ebf19-129">Cuando el asistente muestra la primera página HTML del servidor, lo hace con el conocimiento de los identificadores de las páginas del asistente anteriores y después de las páginas HTML hospedadas.</span><span class="sxs-lookup"><span data-stu-id="ebf19-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="ebf19-130">En este punto del ejemplo, el usuario, sentado en la primera página HTML, hace clic en el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="ebf19-131">El asistente envía una notificación de este evento al servidor.</span><span class="sxs-lookup"><span data-stu-id="ebf19-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="ebf19-132">Al recibir este mensaje, el script de servidor hace referencia a su controlador de **retroceso** para este evento, que, como es la primera página HTML, llama al método **FinalBack** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="ebf19-133">Esto hace que el asistente navegue hasta la página del asistente que se muestra antes de escribir la interfaz de usuario del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="ebf19-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="ebf19-134">Para obtener una descripción completa de estos métodos y propiedades, vea la documentación de los objetos [**WebWizardHost**](/windows/desktop/shell/webwizardhost) y [**NewWDEvents**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="ebf19-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="ebf19-135">Consideraciones de diseño</span><span class="sxs-lookup"><span data-stu-id="ebf19-135">Design Considerations</span></span>

<span data-ttu-id="ebf19-136">El HTML que conforman cada página del servidor se muestra normalmente en el panel del asistente.</span><span class="sxs-lookup"><span data-stu-id="ebf19-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="ebf19-137">Al diseñar estas páginas, tenga en cuenta que no se puede cambiar el tamaño de una ventana del asistente.</span><span class="sxs-lookup"><span data-stu-id="ebf19-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="ebf19-138">Por tanto, las páginas se deben construir y ajustar para que las barras de desplazamiento se eviten siempre que sea posible para proporcionar al usuario una navegación fluida a través del asistente.</span><span class="sxs-lookup"><span data-stu-id="ebf19-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="ebf19-139">Cada página HTML también debe proporcionar un controlador para los eventos **alback**, **alnext** y **OnCancel** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="ebf19-140">El controlador en el **siguiente** control también controlará el evento de **finalización** .</span><span class="sxs-lookup"><span data-stu-id="ebf19-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="ebf19-141">Una página que no implementa una función **alback** se considera no válida y provocará que se muestre una página de error.</span><span class="sxs-lookup"><span data-stu-id="ebf19-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebf19-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebf19-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf19-143">**WebWizardHost**</span><span class="sxs-lookup"><span data-stu-id="ebf19-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="ebf19-144">**NewWDEvents**</span><span class="sxs-lookup"><span data-stu-id="ebf19-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="ebf19-145">Diseño del lado servidor</span><span class="sxs-lookup"><span data-stu-id="ebf19-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 
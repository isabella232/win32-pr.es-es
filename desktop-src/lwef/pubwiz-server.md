---
title: Diseño de Server-Side
description: Las funciones del lado servidor se comunican con el asistente del cliente a través del objeto Windows. external. El script de servidor proporciona estas funciones para responder a los eventos del asistente y para recuperar información acerca del asistente.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- asistentes para publicación, diseño del lado servidor
- Window. external, asistentes para publicación
- asistentes para publicación, Window. external
- asistentes para publicación, funciones de script de navegación
- scripts, asistentes para publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995261"
---
# <a name="server-side-design"></a><span data-ttu-id="c1cd6-109">Diseño de Server-Side</span><span class="sxs-lookup"><span data-stu-id="c1cd6-109">Server-Side Design</span></span>

<span data-ttu-id="c1cd6-110">Las funciones del lado servidor se comunican con el asistente del cliente a través del objeto **Windows. external** .</span><span class="sxs-lookup"><span data-stu-id="c1cd6-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="c1cd6-111">El script de servidor proporciona estas funciones para responder a los eventos del asistente y para recuperar información acerca del asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="c1cd6-112">Los temas siguientes se tratan en este documento.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="c1cd6-113">Implementar funciones de script de navegación</span><span class="sxs-lookup"><span data-stu-id="c1cd6-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="c1cd6-114">Alback ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="c1cd6-115">Siguiente ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="c1cd6-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="c1cd6-117">Otros métodos y propiedades</span><span class="sxs-lookup"><span data-stu-id="c1cd6-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="c1cd6-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1cd6-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="c1cd6-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1cd6-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="c1cd6-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1cd6-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="c1cd6-121">Implementar funciones de script de navegación</span><span class="sxs-lookup"><span data-stu-id="c1cd6-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="c1cd6-122">El script de servidor de cada página HTML responde a los botones de navegación a través de las funciones para **alback**, **Next** y **OnCancel**.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="c1cd6-123">Estas funciones deben ser accesibles a través de **IHTMLDocument:: get \_ script** en el cliente y no toman ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="c1cd6-124">Alback ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-124">OnBack()</span></span>

-   <span data-ttu-id="c1cd6-125">Responde cuando el usuario hace clic en **atrás** en el asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="c1cd6-126">Si la página del servidor actual es la primera página del servidor, llame a **window. external. FinalBack** para indicar al cliente que vaya a la página del lado cliente anterior.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="c1cd6-127">Si la página del servidor actual no es la primera página del servidor, vaya a la página del servidor anterior.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="c1cd6-128">Esta función se debe implementar para cada página.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-128">This function must be implemented for each page.</span></span> <span data-ttu-id="c1cd6-129">Cualquier página que no lo haga, se considera no válida y muestra una página de error.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="c1cd6-130">Siguiente ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-130">OnNext()</span></span>

-   <span data-ttu-id="c1cd6-131">Responde cuando el usuario hace clic en **siguiente** en el asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="c1cd6-132">Si la página del servidor actual es la última página del servidor, llame a **window. external. FinalNext** para indicar al cliente que vaya a la siguiente página del lado cliente o que complete el asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="c1cd6-133">Si la página del servidor actual no es la última página del servidor, vaya a la siguiente página del servidor.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="c1cd6-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="c1cd6-134">OnCancel()</span></span>

-   <span data-ttu-id="c1cd6-135">Responde cuando el usuario hace clic en **Cancelar** en el asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="c1cd6-136">La interfaz de usuario debe estar diseñada para que el usuario pueda cancelar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="c1cd6-137">Una vez que se procesa cualquier procesamiento de la función **OnCancel** , el cliente cierra el asistente.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="c1cd6-138">Otros métodos y propiedades</span><span class="sxs-lookup"><span data-stu-id="c1cd6-138">Other Methods and Properties</span></span>

<span data-ttu-id="c1cd6-139">Se tiene acceso a las funciones implementadas por el cliente a través de **Windows. external**, como son las propiedades.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="c1cd6-140">Los servicios disponibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c1cd6-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="c1cd6-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1cd6-141">Methods</span></span>

-   [<span data-ttu-id="c1cd6-142">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="c1cd6-143">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="c1cd6-144">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="c1cd6-145">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1cd6-145">Properties</span></span>

-   <span data-ttu-id="c1cd6-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1cd6-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="c1cd6-147">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="c1cd6-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="c1cd6-148">En el ejemplo de código siguiente se muestra el código del lado servidor para una página del asistente simple que implementa la página de error del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="c1cd6-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="c1cd6-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1cd6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1cd6-150">Diseño del lado cliente</span><span class="sxs-lookup"><span data-stu-id="c1cd6-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="c1cd6-151">Registrar un servicio</span><span class="sxs-lookup"><span data-stu-id="c1cd6-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 
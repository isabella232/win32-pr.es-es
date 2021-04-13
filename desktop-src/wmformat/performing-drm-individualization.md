---
title: Realización de una individualización DRM
description: Realización de una individualización DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, individualización de DRM
- SDK de Windows Media Format, individualización
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), individualización
- DRM (administración de derechos digitales), individualización
- Administración de derechos digitales (DRM), individualización de DRM
- DRM (administración de derechos digitales), individualización de DRM
- API extendidas del cliente DRM, individualización
- API extendidas de cliente, individualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357531"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="e5830-122">Realización de una individualización DRM</span><span class="sxs-lookup"><span data-stu-id="e5830-122">Performing DRM Individualization</span></span>

<span data-ttu-id="e5830-123">La individualización es el proceso de actualizar el componente DRM en el equipo cliente, cifrarlo y hacerlo único.</span><span class="sxs-lookup"><span data-stu-id="e5830-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="e5830-124">Cuando se crea un equipo, el componente DRM está asociado al equipo y no podrá descodificar el contenido en ningún otro equipo.</span><span class="sxs-lookup"><span data-stu-id="e5830-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="e5830-125">Las API extendidas del cliente DRM de Windows Media ofrecen compatibilidad para la individualización del componente DRM en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="e5830-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="e5830-126">La individualización se realiza llamando al método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="e5830-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="e5830-127">Puede llamar a **PerformSecurityUpdate** para que se pueda individualizar solo si la versión del servidor es más reciente que la instalada en el equipo cliente, o puede forzar la individualización sin tener en cuenta las versiones de seguridad relativas.</span><span class="sxs-lookup"><span data-stu-id="e5830-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="e5830-128">La marca para la individualización necesaria es la seguridad de WMDRM que \_ \_ realiza \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="e5830-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="e5830-129">La marca para la individualización forzada es la seguridad de WMDRM y \_ \_ \_ forzar \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="e5830-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="e5830-130">**PerformSecurityUpdate** es una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e5830-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="e5830-131">Se devolverá rápidamente y después generará eventos para proporcionar información de estado sobre el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="e5830-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="e5830-132">La mayoría de los eventos generados serán eventos **MEWMDRMIndividualizationProgress** y cada uno tiene una interfaz [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="e5830-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="e5830-133">Para obtener la interfaz de estado, debe llamar a **IMFMediaEvent:: GetValue** para recuperar un puntero **IUnknown** que esté en el mismo objeto y, a continuación, consultarlo para **IWMDRMIndividualizationStatus**.</span><span class="sxs-lookup"><span data-stu-id="e5830-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="e5830-134">Puede obtener datos de una estructura [**de \_ \_ Estado**](drmwm-individualize-status.md) de la función de usuario de WM llamando a [**IWMDRMIndividualizeStatus:: getStatus**](iwmdrmindividualizationstatus-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="e5830-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="e5830-135">Cada evento que se genera tiene su propio objeto con estado, por lo que debe seguir el proceso de obtención del valor de evento y la consulta de la interfaz de estado cada vez.</span><span class="sxs-lookup"><span data-stu-id="e5830-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="e5830-136">En función del tamaño de la descarga, puede haber docenas o cientos de eventos **MEWMDRMIndividualizationProgress** .</span><span class="sxs-lookup"><span data-stu-id="e5830-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="e5830-137">Cuando finaliza el proceso de individualización, se genera un evento **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="e5830-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="e5830-138">Cuando se completa la individualización, los únicos objetos existentes que reflejen el nuevo estado de forma individual son los que heredan de [**IWMDRMSecurity**](iwmdrmsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="e5830-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="e5830-139">No se actualizarán todos los demás objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="e5830-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="e5830-140">Debe liberar y volver a crear los demás objetos para que reflejen el nuevo estado de forma individual.</span><span class="sxs-lookup"><span data-stu-id="e5830-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5830-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5830-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5830-142">**Ejemplo de individualización de DRM**</span><span class="sxs-lookup"><span data-stu-id="e5830-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="e5830-143">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="e5830-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e5830-144">**Usar el modelo de eventos Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="e5830-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="e5830-145">[Prácticas recomendadas para la individualización de DRM de Windows Media](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e5830-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 





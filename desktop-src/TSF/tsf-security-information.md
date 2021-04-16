---
title: Consideraciones de seguridad marco de trabajo de servicios de texto
description: Consideraciones de seguridad marco de trabajo de servicios de texto
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Marco de trabajo de servicios de texto (TSF), seguridad
- TSF (marco de trabajo de servicios de texto), seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad para TSF
- Marco de trabajo de servicios de texto (TSF), procedimientos recomendados
- TSF (marco de trabajo de servicios de texto), procedimientos recomendados
- Aplicaciones habilitadas para TSF, procedimientos recomendados
- servicios de texto, procedimientos recomendados
- prácticas recomendadas para TSF
- Marco de trabajo de servicios de texto (TSF), comprobación de errores
- TSF (marco de trabajo de servicios de texto), comprobación de errores
- Aplicaciones habilitadas para TSF, comprobación de errores
- servicios de texto, comprobación de errores
- comprobación de errores
- Text Services Framework (TSF), firmas digitales
- TSF (marco de trabajo de servicios de texto), firmas digitales
- servicios de texto, firmas digitales
- Aplicaciones habilitadas para TSF, firmas digitales
- Firmas digitales
- Text Services Framework (TSF), llamadas LoadLibrary
- TSF (marco de trabajo de servicios de texto), llamadas LoadLibrary
- servicios de texto, llamadas LoadLibrary
- Aplicaciones habilitadas para TSF, llamadas LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685722"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="d2a43-127">Consideraciones de seguridad: marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="d2a43-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="d2a43-128">Prácticas recomendadas para el desarrollo con TSF</span><span class="sxs-lookup"><span data-stu-id="d2a43-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="d2a43-129">**Firmas digitales:** Los proveedores de servicios de texto deben proporcionar firmas digitales con sus ejecutables binarios.</span><span class="sxs-lookup"><span data-stu-id="d2a43-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="d2a43-130">Un servicio de texto registrado tiene acceso a los subprocesos del sistema y podría exponer información que de otro modo no sería accesible.</span><span class="sxs-lookup"><span data-stu-id="d2a43-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="d2a43-131">Para ayudar a garantizar una operación estable y segura, el usuario debe comprobar la firma digital de un servicio de texto antes de que el servicio de texto pueda cargarse.</span><span class="sxs-lookup"><span data-stu-id="d2a43-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="d2a43-132">Consulte [Introduction to Code Signing (introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) ) para obtener el procedimiento adecuado para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="d2a43-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="d2a43-133">**Comprobación de errores:** Se debe comprobar si se ha realizado correctamente cada llamada de método o función.</span><span class="sxs-lookup"><span data-stu-id="d2a43-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="d2a43-134">En caso de error, se deben omitir las llamadas a funciones o métodos restantes.</span><span class="sxs-lookup"><span data-stu-id="d2a43-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="d2a43-135">La mayoría de los ejemplos de código de esta documentación tienen una comprobación de errores limitada, o ninguno, para evitar que se oculte el punto.</span><span class="sxs-lookup"><span data-stu-id="d2a43-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="d2a43-136">No debe pegar los ejemplos de la documentación directamente en el código de producción. en su lugar, debe mejorar los ejemplos agregando su propia comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="d2a43-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="d2a43-137">**Llamadas LoadLibrary:** Para obtener un puntero a cualquiera de las [funciones de TSF](text-services-framework-functions.md), deberá utilizar [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="d2a43-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="d2a43-138">Sin embargo, es importante seguir los procedimientos para dar formato al nombre de la ruta de acceso del archivo DLL, como se indica en la documentación de **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="d2a43-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2a43-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2a43-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2a43-140">Prácticas recomendadas de seguridad</span><span class="sxs-lookup"><span data-stu-id="d2a43-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="d2a43-141">[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2a43-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2a43-142">Funciones de TSF</span><span class="sxs-lookup"><span data-stu-id="d2a43-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="d2a43-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="d2a43-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="d2a43-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="d2a43-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
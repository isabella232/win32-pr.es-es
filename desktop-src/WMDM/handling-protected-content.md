---
title: Control de contenido protegido
description: Control de contenido protegido
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- aplicaciones de escritorio, certificados
- proveedores de servicios, certificados
- Guía de programación, certificados
- certificates
- Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- Administrador de dispositivos, proveedor de contenido seguro (SCP)
- aplicaciones de escritorio, proveedor de contenido seguro (SCP)
- proveedores de servicios, proveedor de contenido seguro (SCP)
- Guía de programación, proveedor de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- aplicaciones de escritorio, contenido protegido con DRM
- proveedores de servicios, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418561"
---
# <a name="handling-protected-content"></a><span data-ttu-id="a4a11-122">Control de contenido protegido</span><span class="sxs-lookup"><span data-stu-id="a4a11-122">Handling Protected Content</span></span>

<span data-ttu-id="a4a11-123">Si va a crear una aplicación o un proveedor de servicios que consume contenido protegido por la administración de derechos digitales (DRM) de Windows Media, debe tener un par de claves/certificados emitidos por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a4a11-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="a4a11-124">Para obtener información sobre dónde obtener este certificado, vea [herramientas para el desarrollo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="a4a11-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="a4a11-125">Si no desea controlar el contenido protegido, puede usar la clave ficticia y el certificado proporcionado con este SDK en un archivo denominado Key. c.</span><span class="sxs-lookup"><span data-stu-id="a4a11-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="a4a11-126">En el caso de cualquier archivo que esté protegido por la tecnología DRM, Windows Media Administrador de dispositivos requiere la presencia de un proveedor de contenido seguro (SCP) para ese formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="a4a11-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="a4a11-127">Microsoft proporciona un módulo SCP para archivos WMA y WMV.</span><span class="sxs-lookup"><span data-stu-id="a4a11-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="a4a11-128">Si su aplicación o proveedor de servicios va a controlar el contenido protegido con DRM de otro formato, debe proporcionar su propio módulo SCP.</span><span class="sxs-lookup"><span data-stu-id="a4a11-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="a4a11-129">Un módulo SCP es un objeto COM que implementa todas las [interfaces para los proveedores de contenido seguros](interfaces-for-secure-content-providers.md).</span><span class="sxs-lookup"><span data-stu-id="a4a11-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="a4a11-130">Una aplicación puede enviar contenido protegido con DRM a dispositivos basados en Windows Media DRM 10 para dispositivos portátiles o DRM de dispositivo portátil (PDDRM).</span><span class="sxs-lookup"><span data-stu-id="a4a11-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="a4a11-131">Sin embargo, solo puede crear un proveedor de servicios para dispositivos basados en PDDRM; no se puede crear un proveedor de servicios para dispositivos integrados en Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="a4a11-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="a4a11-132">Estos últimos dispositivos solo pueden usar el proveedor de servicios MTP proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a4a11-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="a4a11-133">Los dispositivos basados en PDDRM solo admiten licencias para contenido adquirido.</span><span class="sxs-lookup"><span data-stu-id="a4a11-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="a4a11-134">Las licencias que tienen condiciones de expiración de tiempo solo se admiten en dispositivos basados en Windows Media DRM 10 para dispositivos portátiles, que tienen requisitos especiales, como un reloj seguro y una individualización.</span><span class="sxs-lookup"><span data-stu-id="a4a11-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="a4a11-135">El SDK de Windows Media DRM 10 para dispositivos portátiles ofrece detalles sobre los requisitos de los dispositivos para admitir la tecnología de la versión 10.</span><span class="sxs-lookup"><span data-stu-id="a4a11-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="a4a11-136">Antes de enviar contenido DRM al dispositivo, una aplicación debe comprobar varias cosas:</span><span class="sxs-lookup"><span data-stu-id="a4a11-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="a4a11-137">Que el dispositivo admita la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="a4a11-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="a4a11-138">Qué versión de la tecnología DRM es compatible (versión 10 o anterior).</span><span class="sxs-lookup"><span data-stu-id="a4a11-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="a4a11-139">Si el dispositivo se basa en la versión 10, todos sus componentes están actualizados (como el reloj seguro y los requisitos de individualización).</span><span class="sxs-lookup"><span data-stu-id="a4a11-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="a4a11-140">Todas las llamadas a métodos para responder a estas preguntas las realiza el cliente y las controla Windows Media Administrador de dispositivos y el componente de proveedor de contenido seguro. el proveedor de servicios no controla ninguna de estas llamadas.</span><span class="sxs-lookup"><span data-stu-id="a4a11-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="a4a11-141">Si el dispositivo no es compatible con DRM 10 de Windows Media para dispositivos portátiles, es posible que siga pudiendo consumir contenido protegido (en función de la licencia de contenido y el diseño del dispositivo), pero cualquier contenido que se le envíe tendrá una licencia de uso simplificada con derechos limitados (por ejemplo, sin expiración de tiempo).</span><span class="sxs-lookup"><span data-stu-id="a4a11-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="a4a11-142">Para obtener ejemplos en los que se muestra cómo una aplicación comprueba si un dispositivo puede controlar contenido protegido y si es necesario actualizar sus componentes de DRM, consulte [Administración del contenido protegido en la aplicación](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="a4a11-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="a4a11-143">Para obtener más información acerca de la creación de un proveedor de servicios que pueda controlar el contenido protegido, consulte [control del contenido protegido en el proveedor de servicios](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a4a11-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="a4a11-144">Muchos métodos de transferencia de archivos de Windows Media Administrador de dispositivos o de solicitud de derechos producirán un error (a menudo con un valor **HRESULT** misterioso) al administrar archivos protegidos con DRM con un depurador adjunto.</span><span class="sxs-lookup"><span data-stu-id="a4a11-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="a4a11-145">Por lo tanto, debe usar formas alternativas para depurar el código, como el registro de salidas en un archivo de registro o de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="a4a11-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="a4a11-146">Para obtener más información sobre las opciones de registro, vea [Habilitar el registro](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="a4a11-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="a4a11-147">Si está ejecutando un depurador en contenido protegido, un método devolverá uno de los códigos de error enumerados en los [códigos de error](error-codes.md)de la sección DRM o, posiblemente, un código de error desconocido.</span><span class="sxs-lookup"><span data-stu-id="a4a11-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="a4a11-148">Si obtiene valores **HRESULT** misteriosas al ejecutar un depurador en métodos o contenido protegido, la protección DRM podría ser la causa.</span><span class="sxs-lookup"><span data-stu-id="a4a11-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a4a11-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4a11-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a11-150">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="a4a11-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





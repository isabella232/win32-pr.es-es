---
title: Herramientas para desarrollo
description: Herramientas para desarrollo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Administrador de dispositivos, herramientas de desarrollo
- Administrador de dispositivos, herramientas de desarrollo
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Administrador de dispositivos de Windows Media, claves
- Administrador de dispositivos, claves
- Windows Media Administrador de dispositivos, bibliotecas
- Administrador de dispositivos, bibliotecas
- Windows Media Administrador de dispositivos, kit de desarrollo de software (SDK)
- Administrador de dispositivos, kit de desarrollo de software (SDK)
- SDK de Administrador de dispositivos de Windows Media
- SDK de Administrador de dispositivos
- SDK de Media Player de Windows
- SDK de Windows Media Format
- SDK de Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105695794"
---
# <a name="tools-for-development"></a><span data-ttu-id="77418-118">Herramientas para desarrollo</span><span class="sxs-lookup"><span data-stu-id="77418-118">Tools for Development</span></span>

<span data-ttu-id="77418-119">En esta sección se describen los distintos certificados y claves, bibliotecas y SDK que se deben programar con el SDK de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="77418-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="77418-120">Certificados y claves</span><span class="sxs-lookup"><span data-stu-id="77418-120">Certificates and Keys</span></span>

<span data-ttu-id="77418-121">El SDK de Windows Media Administrador de dispositivos incluye un par de claves/certificados de prueba (en el archivo Key. c) que puede usar una aplicación o un proveedor de servicios para usar los métodos de Administrador de dispositivos de Windows Media en contenido no protegido.</span><span class="sxs-lookup"><span data-stu-id="77418-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="77418-122">Este par de clave y certificado permite que la aplicación o el proveedor de servicios usen la mayor parte de la funcionalidad de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="77418-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="77418-123">Sin embargo, para desarrollar una aplicación o un proveedor de servicios que pueda controlar contenido protegido con DRM, debe solicitar uno o más certificados (cada uno con una clave) de la [Página de licencias de Windows Media](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="77418-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="77418-124">Los certificados son necesarios para las siguientes aplicaciones u objetos:</span><span class="sxs-lookup"><span data-stu-id="77418-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="77418-125">Los proveedores de servicios que controlan contenido protegido con DRM requieren un certificado (y una clave) de proveedor de servicios de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="77418-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="77418-126">Las aplicaciones que transfieren contenido protegido con DRM requieren un certificado (y una clave) de Windows Media Administrador de dispositivos Transfer</span><span class="sxs-lookup"><span data-stu-id="77418-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="77418-127">Las aplicaciones que reproducen contenido protegido con DRM requieren un certificado DRM (y una clave).</span><span class="sxs-lookup"><span data-stu-id="77418-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="77418-128">Los componentes de medición de licencias requieren un certificado de medición.</span><span class="sxs-lookup"><span data-stu-id="77418-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="77418-129">Lo proporciona un servicio de medición de licencias basado en el SDK de Windows Media Rights Manager, que se puede solicitar en la página de administración de licencias de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="77418-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="77418-130">Encabezados y bibliotecas</span><span class="sxs-lookup"><span data-stu-id="77418-130">Libraries and Headers</span></span>

<span data-ttu-id="77418-131">Además de las bibliotecas y los encabezados que se mencionan en [los archivos de encabezado y biblioteca necesarios para una aplicación](required-library-and-header-files-for-an-application.md) o las [bibliotecas y encabezados necesarios para un proveedor de servicios](required-libraries-and-headers-for-a-service-provider.md), cualquier aplicación o complemento que anteriormente se vinculó a WMDRMSDK. lib para llamar a las funciones del SDK de Windows Media Format debe estar vinculado ahora a WMDRMSDKStub. lib.</span><span class="sxs-lookup"><span data-stu-id="77418-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="77418-132">Este archivo de biblioteca se usa para tener acceso a archivos protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="77418-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="77418-133">También puede solicitar esta biblioteca desde la página de licencias de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="77418-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="77418-134">SDK relacionados</span><span class="sxs-lookup"><span data-stu-id="77418-134">Related SDKs</span></span>

<span data-ttu-id="77418-135">Los siguientes SDK de Microsoft proporcionan elementos que puede necesitar para diseñar soluciones para dispositivos multimedia portátiles.</span><span class="sxs-lookup"><span data-stu-id="77418-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="77418-136">Se requiere SDK</span><span class="sxs-lookup"><span data-stu-id="77418-136">SDK Required</span></span>                     | <span data-ttu-id="77418-137">Requerido para...</span><span class="sxs-lookup"><span data-stu-id="77418-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77418-138">SDK de Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="77418-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="77418-139">Aplicaciones del reproductor multimedia de escritorio que se comunican con dispositivos portátiles</span><span class="sxs-lookup"><span data-stu-id="77418-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="77418-140">Aplicaciones de escritorio que pueden intercambiar archivos o información con dispositivos portátiles</span><span class="sxs-lookup"><span data-stu-id="77418-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="77418-141">Windows Media Player medición de objetos COM</span><span class="sxs-lookup"><span data-stu-id="77418-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="77418-142">SDK de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="77418-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="77418-143">Complementos de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="77418-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="77418-144">Windows Media Player medición de objetos COM</span><span class="sxs-lookup"><span data-stu-id="77418-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="77418-145">Máscaras de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="77418-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="77418-146">SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="77418-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="77418-147">Reproductores de audio o vídeo que pueden crear o reproducir archivos (especialmente archivos ASF)</span><span class="sxs-lookup"><span data-stu-id="77418-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="77418-148">Aplicaciones de edición de audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="77418-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="77418-149">SDK de Windows Media Rights Manager</span><span class="sxs-lookup"><span data-stu-id="77418-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="77418-150">Las aplicaciones o los complementos que se reproducen en el equipo de escritorio o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77418-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="77418-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77418-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77418-152">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="77418-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 






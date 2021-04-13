---
title: Listas de inclusión y autorización explícitas
description: Listas de inclusión y autorización explícitas
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- SDK de Windows Media Format, exportación de DRM
- SDK de Windows Media Format, exportar
- SDK de Windows Media Format, listas de autorización e inclusión explícitas
- SDK de Windows Media Format, listas de autorización
- SDK de Windows Media Format, listas de inclusión
- Administración de derechos digitales (DRM), exportar
- DRM (administración de derechos digitales), exportar
- Administración de derechos digitales (DRM), listas de inclusión y autorización explícitas
- DRM (administración de derechos digitales), listas de inclusión y autorización explícitas
- Administración de derechos digitales (DRM), listas de autorización
- DRM (administración de derechos digitales), listas de autorización
- Administración de derechos digitales (DRM), listas de inclusión
- DRM (administración de derechos digitales), listas de inclusión
- API extendidas del cliente DRM, listas de inclusión y autorización explícitas
- API extendidas de cliente, listas de autorización e inclusión explícitas
- API extendidas del cliente DRM, listas de autorización
- API extendidas de cliente, listas de autorización
- API extendidas del cliente DRM, listas de inclusión
- API extendidas de cliente, listas de inclusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420247"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="ede35-122">Listas de inclusión y autorización explícitas</span><span class="sxs-lookup"><span data-stu-id="ede35-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="ede35-123">Las licencias pueden contener una lista de inclusión para autorizar explícitamente la exportación de contenido protegido por DRM de Windows Media a otros esquemas de protección de contenido (CPS).</span><span class="sxs-lookup"><span data-stu-id="ede35-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="ede35-124">Según los términos del contrato de licencia que escriba en con Microsoft para habilitar la exportación de DRM, solo puede exportar a una CPS válida que se identifique en la lista de inclusión de una licencia.</span><span class="sxs-lookup"><span data-stu-id="ede35-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="ede35-125">Una lista de inclusión es una matriz delimitada de identificadores únicos globales (GUID) que representa una CPS autorizada específica a la que se puede exportar el contenido.</span><span class="sxs-lookup"><span data-stu-id="ede35-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="ede35-126">Los GUID que aparecen en una lista de inclusión son independientes de los niveles de protección de salida (OPL) y los niveles de protección de contenido (CPL).</span><span class="sxs-lookup"><span data-stu-id="ede35-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="ede35-127">Aplicar estas restricciones es responsabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ede35-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="ede35-128">Cuando se realiza la exportación de DRM de Windows Media en el contenido comprimido, se obtiene acceso a la lista de inclusión a través del método [**IWMDRMLicense:: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) .</span><span class="sxs-lookup"><span data-stu-id="ede35-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="ede35-129">Al realizar la exportación de DRM de Windows Media en el contenido sin comprimir, use el método [**IWMDRMReader3:: GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .</span><span class="sxs-lookup"><span data-stu-id="ede35-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="ede35-130">Para registrar un nuevo sistema de protección de contenido como una exportación permitida de DRM de Windows Media en las reglas de compatibilidad de exportación de DRM de Windows Media, póngase en contacto con wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="ede35-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ede35-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ede35-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede35-132">**Exportación de DRM**</span><span class="sxs-lookup"><span data-stu-id="ede35-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 





---
title: Interfaces para proveedores de contenido seguros
description: Interfaces para proveedores de contenido seguros
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- referencia de programación, contenido protegido con DRM
- referencia de Windows Media Administrador de dispositivos, contenido protegido con DRM
- Contenido protegido con DRM
- Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- Administrador de dispositivos, proveedor de contenido seguro (SCP)
- referencia de programación, proveedor de contenido seguro (SCP)
- referencia de Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Media Administrador de dispositivos, interfaces SCP
- Administrador de dispositivos, interfaces SCP
- referencia de programación, interfaces SCP
- referencia de Windows Media Administrador de dispositivos, interfaces SCP
- Interfaces SCP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695338"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="a8e47-119">Interfaces para proveedores de contenido seguros</span><span class="sxs-lookup"><span data-stu-id="a8e47-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="a8e47-120">Un proveedor de contenido seguro (SCP) es un componente de complemento que permite a Windows Media Administrador de dispositivos transferir y solicitar información de derechos del contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="a8e47-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="a8e47-121">Microsoft proporciona un componente SCP que puede controlar archivos WMA y WMV protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="a8e47-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="a8e47-122">Si el dispositivo o la aplicación usarán contenido protegido con DRM de otros formatos, debe crear un componente SCP implementando todas estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="a8e47-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="a8e47-123">De lo contrario, no tendrá que utilizar estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="a8e47-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="a8e47-124">Interfaz</span><span class="sxs-lookup"><span data-stu-id="a8e47-124">Interface</span></span>                                                  | <span data-ttu-id="a8e47-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8e47-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8e47-126">**ISCPSecureAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="a8e47-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="a8e47-127">La interfaz principal del proveedor de contenido seguro.</span><span class="sxs-lookup"><span data-stu-id="a8e47-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="a8e47-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="a8e47-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="a8e47-129">Extiende **ISCPSecureAuthenticate** proporcionando una manera de obtener un objeto de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8e47-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="a8e47-130">**ISCPSecureExchange**</span><span class="sxs-lookup"><span data-stu-id="a8e47-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="a8e47-131">Se usa para intercambiar el contenido protegido y los derechos asociados con el contenido.</span><span class="sxs-lookup"><span data-stu-id="a8e47-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="a8e47-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="a8e47-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="a8e47-133">Extiende **ISCPSecureExchange** proporcionando una nueva versión del método **TransferContainerData** .</span><span class="sxs-lookup"><span data-stu-id="a8e47-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="a8e47-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="a8e47-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="a8e47-135">Extiende **ISCPSecureExchange2** proporcionando un mejor rendimiento de intercambio de datos y un método de devolución de llamada completo de transferencia.</span><span class="sxs-lookup"><span data-stu-id="a8e47-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="a8e47-136">**ISCPSecureQuery**</span><span class="sxs-lookup"><span data-stu-id="a8e47-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="a8e47-137">Lo consulta Windows Media Administrador de dispositivos para determinar la propiedad del contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="a8e47-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="a8e47-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="a8e47-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="a8e47-139">Extiende **ISCPSecureQuery** a través de la funcionalidad que determina si el proveedor de contenido seguro es responsable del contenido y, en tal caso, proporciona una dirección URL para actualizar los componentes revocados y determinar qué componentes se han revocado.</span><span class="sxs-lookup"><span data-stu-id="a8e47-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="a8e47-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="a8e47-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="a8e47-141">Extiende **ISCPSecureQuery2** proporcionando un conjunto de nuevos métodos para recuperar los derechos y tomar decisiones sobre un canal claro.</span><span class="sxs-lookup"><span data-stu-id="a8e47-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="a8e47-142">**ISCPSession**</span><span class="sxs-lookup"><span data-stu-id="a8e47-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="a8e47-143">Proporciona una administración de Estado común y eficaz para varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="a8e47-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 





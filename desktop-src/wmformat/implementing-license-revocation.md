---
title: Implementación de la revocación de licencias
description: Implementación de la revocación de licencias
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- SDK de Windows Media Format, implementar la revocación de licencias
- SDK de Windows Media Format, revocación de licencia
- SDK de Windows Media Format, revocación de licencias
- Advanced Systems Format (ASF), implementación de la revocación de licencias
- ASF (formato de sistemas avanzados), implementación de la revocación de licencias
- Advanced Systems Format (ASF), revocación de licencia
- ASF (formato de sistemas avanzados), revocación de licencia
- Advanced Systems Format (ASF), revocación de licencias
- ASF (formato de sistemas avanzados), revocación de licencias
- Administración de derechos digitales (DRM), implementación de la revocación de licencias
- DRM (administración de derechos digitales), implementación de la revocación de licencias
- Administración de derechos digitales (DRM), revocación de licencia
- DRM (administración de derechos digitales), revocación de licencia
- Administración de derechos digitales (DRM), revocación de licencias
- DRM (administración de derechos digitales), revocación de licencias
- revocación de licencias, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788817"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="e8a59-119">Implementación de la revocación de licencias</span><span class="sxs-lookup"><span data-stu-id="e8a59-119">Implementing License Revocation</span></span>

<span data-ttu-id="e8a59-120">El SDK de Windows Media Rights Manager 10 incluye una característica denominada revocación de licencia.</span><span class="sxs-lookup"><span data-stu-id="e8a59-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="e8a59-121">Esta característica permite que los servidores de licencias soliciten que se quiten las licencias del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="e8a59-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="e8a59-122">El SDK de Windows Media Format proporciona métodos que procesan los mensajes de revocación y quitan las licencias del almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="e8a59-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="e8a59-123">Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="e8a59-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="e8a59-124">La aplicación puede hospedar este servicio o puede ser una aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="e8a59-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="e8a59-125">En cualquier caso, la aplicación debe ser capaz de recibir un desafío de licencia creado por el servicio.</span><span class="sxs-lookup"><span data-stu-id="e8a59-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="e8a59-126">Para quitar licencias del almacén de licencias, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8a59-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="e8a59-127">Tras recibir un desafío de licencia del emisor de la licencia, llame a la función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) para crear un objeto de agente de revocación de licencias y obtener un puntero a la interfaz [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="e8a59-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="e8a59-128">Llame al método [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) para generar la respuesta de desafío.</span><span class="sxs-lookup"><span data-stu-id="e8a59-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="e8a59-129">Vuelva a enviar la respuesta de desafío al componente del servicio de licencias desde el que recibió el desafío.</span><span class="sxs-lookup"><span data-stu-id="e8a59-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="e8a59-130">El componente del servicio de licencias envía un BLOB de revocación de licencia (LRB) firmado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8a59-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="e8a59-131">Cuando lo reciba, llame al método [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) .</span><span class="sxs-lookup"><span data-stu-id="e8a59-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="e8a59-132">**ProcessLRB** crea un mensaje de confirmación que debe devolver al servicio de licencias para comprobar que se han quitado las licencias.</span><span class="sxs-lookup"><span data-stu-id="e8a59-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="e8a59-133">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="e8a59-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e8a59-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8a59-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a59-135">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="e8a59-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="e8a59-136">**Interfaz IWMLicenseRevocationAgent**</span><span class="sxs-lookup"><span data-stu-id="e8a59-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 





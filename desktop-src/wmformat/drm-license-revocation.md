---
title: Revocación de licencia (cliente DRM de Microsoft Windows Media)
description: Revocación de licencia (cliente DRM de Microsoft Windows Media)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, revocación de licencia
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), revocación de licencia
- DRM (administración de derechos digitales), revocación de licencia
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, revocación de licencia
- API extendidas de cliente, revocación de licencia
- licencias, revocación
- revocación de licencias, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279734"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="3131a-115">Revocación de licencia (cliente DRM de Microsoft Windows Media)</span><span class="sxs-lookup"><span data-stu-id="3131a-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="3131a-116">La revocación de licencias hace referencia a la eliminación de licencias de un almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="3131a-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="3131a-117">Un escenario común para la revocación de licencias se produce cuando un proveedor de servicios, como un servicio de suscripción de música, debe desactivar el servicio en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3131a-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="3131a-118">Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="3131a-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="3131a-119">La aplicación puede hospedar este servicio o puede ser una aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="3131a-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="3131a-120">En cualquier caso, la aplicación debe ser capaz de recibir un desafío de licencia creado por el servicio.</span><span class="sxs-lookup"><span data-stu-id="3131a-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="3131a-121">Para quitar licencias del almacén de licencias, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3131a-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="3131a-122">Tras recibir un desafío de licencia del emisor de la licencia, cree un desafío de revocación mediante el método [**IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="3131a-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="3131a-123">Este método asignará un búfer que contiene los datos de un desafío de revocación, que se pasa a la aplicación a través del parámetro *ppbChallengeOutput* .</span><span class="sxs-lookup"><span data-stu-id="3131a-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="3131a-124">Envíe el desafío de revocación de licencias a un servicio de revocación de licencias.</span><span class="sxs-lookup"><span data-stu-id="3131a-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="3131a-125">El servidor generará un BLOB de revocación de licencias (LRB) en respuesta.</span><span class="sxs-lookup"><span data-stu-id="3131a-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="3131a-126">Quite la licencia del almacén local mediante el método [**IWMDRMLicenseManagement::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , pasando el LRB devuelto por el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="3131a-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="3131a-127">Desasigne el búfer asignado por **CreateLicenseRevocationChallenge** mediante la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="3131a-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="3131a-128">Para obtener más información sobre cómo funciona la revocación de licencias o sobre cómo escribir un servicio de revocación, consulte implementación de la [revocación de licencias](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span><span class="sxs-lookup"><span data-stu-id="3131a-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3131a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3131a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3131a-130">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="3131a-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="3131a-131">**Almacén de licencias local**</span><span class="sxs-lookup"><span data-stu-id="3131a-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="3131a-132">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="3131a-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 
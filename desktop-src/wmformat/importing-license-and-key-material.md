---
title: Importación de la licencia y el material de clave
description: Importación de la licencia y el material de clave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), material de clave
- DRM (administración de derechos digitales), material de clave
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, material de clave
- API extendidas de cliente, material de clave
- licencias, importar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269320"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="6a086-119">Importación de la licencia y el material de clave</span><span class="sxs-lookup"><span data-stu-id="6a086-119">Importing License and Key Material</span></span>

<span data-ttu-id="6a086-120">Si tiene contenido multimedia que se cifró mediante un sistema de protección de contenido de terceros y desea importar la licencia y el material de clave en DRM de Windows Media, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6a086-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="6a086-121">Recupere la colección de certificados de la máquina DRM de Windows Media llamando al método [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="6a086-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="6a086-122">Analice la colección de certificados, asegurándose de que se firmó correctamente y se valide a una clave pública raíz conocida de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6a086-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="6a086-123">La colección de certificados se ajusta al esquema XMR.</span><span class="sxs-lookup"><span data-stu-id="6a086-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="6a086-124">Para obtener más información, consulte [Building a XMR License](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="6a086-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="6a086-125">Opcional: Extraiga la lista de revocación llamando al método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6a086-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="6a086-126">Opcional: Asegúrese de que no se revoca ningún certificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="6a086-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="6a086-127">Para obtener más información, consulte Comprobación de la [revocación de certificados](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="6a086-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="6a086-128">Genere una licencia en el formato XMR que represente los requisitos de la Directiva para el contenido de importación y contenga el material de clave DRM de Windows Media adecuado.</span><span class="sxs-lookup"><span data-stu-id="6a086-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="6a086-129">Para obtener más información, vea el tema [Building a XMR License](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="6a086-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="6a086-130">Pase la licencia de XMR al sistema DRM de Windows Media para su procesamiento, mediante el método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="6a086-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="6a086-131">Los detalles sobre el esquema XMR se le proporcionarán al conceder licencias de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6a086-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6a086-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a086-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a086-133">**Comprobación de la revocación de certificados**</span><span class="sxs-lookup"><span data-stu-id="6a086-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="6a086-134">**Creación de una licencia de XMR**</span><span class="sxs-lookup"><span data-stu-id="6a086-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="6a086-135">**Importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="6a086-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 





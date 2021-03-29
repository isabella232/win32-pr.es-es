---
title: Exportar contenido comprimido
description: Exportar contenido comprimido
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- SDK de Windows Media Format, exportación de DRM
- SDK de Windows Media Format, exportar
- SDK de Windows Media Format, contenido comprimido
- Administración de derechos digitales (DRM), exportar
- DRM (administración de derechos digitales), exportar
- Administración de derechos digitales (DRM), contenido comprimido
- DRM (administración de derechos digitales), contenido comprimido
- API extendidas del cliente DRM, contenido comprimido
- API extendidas de cliente, contenido comprimido
- API extendidas del cliente DRM, exportar
- API extendidas del cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903361"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="407ee-114">Exportar contenido comprimido</span><span class="sxs-lookup"><span data-stu-id="407ee-114">Exporting Compressed Content</span></span>

<span data-ttu-id="407ee-115">En esta sección se describe la exportación de medios protegidos con DRM de Windows Media en un archivo de Windows Media en el que la aplicación recibe datos de medios digitales comprimidos.</span><span class="sxs-lookup"><span data-stu-id="407ee-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="407ee-116">Para ello, la aplicación debe realizar el descifrado alineado de todas las cargas cifradas de DRM de Windows Media en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="407ee-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="407ee-117">Se le proporciona una biblioteca de análisis ASF como parte del contrato de exportación DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="407ee-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="407ee-118">Los pasos principales implicados en la exportación de contenido comprimido son:</span><span class="sxs-lookup"><span data-stu-id="407ee-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="407ee-119">Realice una individualización de DRM, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="407ee-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="407ee-120">Compruebe que el esquema de protección de contenido de destino está permitido explícitamente.</span><span class="sxs-lookup"><span data-stu-id="407ee-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="407ee-121">Cree un objeto descifrador para descifrar cada carga de ASF.</span><span class="sxs-lookup"><span data-stu-id="407ee-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="407ee-122">El sistema DRM transmite cada carga ASF de Windows Media DRM a RC4 antes de pasarla a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="407ee-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="407ee-123">Si la aplicación cambia el tamaño de una carga ASF durante el transcifrado, también debe remultiplexar el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="407ee-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="407ee-124">Pase a la biblioteca de código auxiliar un certificado de aplicación de exportación de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="407ee-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="407ee-125">Se comprueba el certificado y, si es válido, el sistema DRM genera un vector de inicialización y lo cifra mediante RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="407ee-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="407ee-126">Se crea una clave de sesión RC4 para cada carga mediante la concatenación del vector de inicialización y un valor Salt.</span><span class="sxs-lookup"><span data-stu-id="407ee-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="407ee-127">Proporcione el valor Salt a la API de descifrado y debe incrementarlo mediante un valor entero positivo distinto de cero para cada carga.</span><span class="sxs-lookup"><span data-stu-id="407ee-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="407ee-128">Microsoft le proporcionará una herramienta como parte del contrato de exportación de Windows Media DRM que le permitirá generar su propio par de claves pública y privada RSA.</span><span class="sxs-lookup"><span data-stu-id="407ee-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="407ee-129">Enviará la clave pública a Microsoft, donde Microsoft la incorporará a un certificado de aplicación DRM de Windows Media firmado y lo devolverá.</span><span class="sxs-lookup"><span data-stu-id="407ee-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="407ee-130">Cada carga, una vez descifrada con la clave de descifrado RC4, debe cifrarse inmediatamente en la CPS de salida.</span><span class="sxs-lookup"><span data-stu-id="407ee-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="407ee-131">Existen otras restricciones en el control de cargas no cifradas que se describen en las reglas de solidez y cumplimiento, que acompañan al contrato de exportación de Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="407ee-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="407ee-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="407ee-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="407ee-133">**Descifrado y recifrado de carga ASF**</span><span class="sxs-lookup"><span data-stu-id="407ee-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="407ee-134">**Exportación de DRM**</span><span class="sxs-lookup"><span data-stu-id="407ee-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="407ee-135">**Realización de una individualización DRM**</span><span class="sxs-lookup"><span data-stu-id="407ee-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="407ee-136">**Comprobación e inicialización**</span><span class="sxs-lookup"><span data-stu-id="407ee-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 





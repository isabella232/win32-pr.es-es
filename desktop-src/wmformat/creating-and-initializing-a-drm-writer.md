---
title: Creación e inicialización de un escritor DRM
description: Creación e inicialización de un escritor DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- SDK de Windows Media Format, escritores de DRM
- Administración de derechos digitales (DRM), creación de escritores DRM
- DRM (administración de derechos digitales), creación de escritores DRM
- Administración de derechos digitales (DRM), inicializando escritores de DRM
- DRM (administración de derechos digitales), inicializar escritores de DRM
- API extendidas del cliente DRM, escritores de DRM
- API extendidas de cliente, escritores de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105705063"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="8cd8c-110">Creación e inicialización de un escritor DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="8cd8c-111">Los pasos siguientes son necesarios para inicializar un objeto de escritor ASF para importar ejemplos de medios cifrados en Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="8cd8c-112">Siga los pasos del 1 al 4 de importación de la [licencia y el material de clave](importing-license-and-key-material.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="8cd8c-113">Cree e inicialice un objeto de escritura ASF con el material de clave DRM de Windows Media adecuado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="8cd8c-114">Para obtener más información, consulte [Habilitar la compatibilidad con DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="8cd8c-115">Establezca cada uno de los atributos siguientes llamando a [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span><span class="sxs-lookup"><span data-stu-id="8cd8c-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="8cd8c-116">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="8cd8c-117">\_V1LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="8cd8c-118">ID. de ID \_ de DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="8cd8c-119">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="8cd8c-120">Si una versión con licencia de Windows Media Rights Manager no está instalada en el equipo que ejecuta el software, también se deben establecer los cuatro atributos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8cd8c-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="8cd8c-121">\_LASIGNATUREROOTCERT DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="8cd8c-122">\_LASIGNATURECERT DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="8cd8c-123">\_LASIGNATURELICSRVCERT DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="8cd8c-124">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="8cd8c-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="8cd8c-125">La aplicación para los certificados de cifrado necesarios se puede completar rellenando el [contrato de licencia de Windows Media (WMLA)](https://www.microsoft.com/licensing/default) en línea.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="8cd8c-126">Cree una clave de sesión y rellene una estructura de claves de la [**\_ sesión de importación de \_ \_ WMDRM**](wmdrm-import-session-key.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="8cd8c-127">La clave de sesión se utilizará para cifrar una clave de contenido.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="8cd8c-128">Para obtener un ejemplo, consulte el ejemplo de cómo [crear una clave de sesión](create-session-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="8cd8c-129">Cree una clave de contenido a partir de un vector de inicialización de RC4 aleatorio y rellene una estructura de [**clave de contenido de importación de WMDRM \_ \_ \_**](wmdrm-import-content-key.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="8cd8c-130">La clave de contenido se usa para cifrar los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="8cd8c-131">Para obtener un ejemplo, consulte el ejemplo de creación de una [clave de contenido](create-content-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="8cd8c-132">Cifre la clave de contenido con la clave de sesión mediante el cifrado RC4.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="8cd8c-133">Extraiga la clave de la colección de certificados de la máquina.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="8cd8c-134">Para obtener un ejemplo, consulte [Get Machine Certificate example](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="8cd8c-135">Cifre la clave de sesión con la clave pública extraída del certificado.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="8cd8c-136">Rellene una estructura de struct de la [**\_ importación del \_ inicializador \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="8cd8c-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="8cd8c-137">Llame al método [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) para notificar al SDK que los ejemplos que entran en el escritor ya están protegidos y deben enviarse directamente al cliente DRM de Windows Media para la importación.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="8cd8c-138">Llame a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="8cd8c-139">El resto de los pasos para crear un archivo protegido con DRM se documentan en la guía de programación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="8cd8c-140">Para obtener más información, vea [crear archivos protegidos](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="8cd8c-141">El siguiente paso consiste en recorrer en iteración cada ejemplo multimedia, cifrarlo y pasarlo al objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="8cd8c-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="8cd8c-142">Para obtener más información, consulte los [ejemplos de cifrado e importación de medios](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8cd8c-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cd8c-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cd8c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd8c-144">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="8cd8c-145">**Importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="8cd8c-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 





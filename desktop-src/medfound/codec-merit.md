---
description: Mérito del códec
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Mérito del códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558115"
---
# <a name="codec-merit"></a><span data-ttu-id="8bd1b-103">Mérito del códec</span><span class="sxs-lookup"><span data-stu-id="8bd1b-103">Codec Merit</span></span>

<span data-ttu-id="8bd1b-104">A partir de Windows 7, se puede asignar un valor de *mérito* a un códec de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="8bd1b-105">Cuando se enumeran los códecs, se prefieren los códecs con mayores méritos que los códecs con un mérito menor.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="8bd1b-106">Los códecs con cualquier valor de mérito son preferibles a los códecs sin un mérito asignado.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="8bd1b-107">Para obtener más información acerca de la enumeración de códecs, vea [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="8bd1b-108">Los valores de mérito son asignados por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="8bd1b-109">Actualmente, solo los códecs de hardware son válidos para recibir un valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="8bd1b-110">El proveedor del códec también emite un certificado digital, que se usa para comprobar el valor de mérito del códec.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="8bd1b-111">Para obtener un certificado, envíe una solicitud de correo electrónico a wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="8bd1b-112">El proceso para obtener un certificado incluye firmar una licencia y proporcionar un conjunto de archivos de información a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="8bd1b-113">El mérito del códec funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="8bd1b-114">El proveedor del códec implementa una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="8bd1b-115">Un controlador AVStream.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-115">An AVStream mini-driver.</span></span> <span data-ttu-id="8bd1b-116">Media Foundation proporciona una MFT de proxy estándar para los controladores AVStream.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="8bd1b-117">Ésta es la opción recomendada.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="8bd1b-118">Una transformación de Media Foundation (MFT) que actúa como proxy en el hardware.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="8bd1b-119">Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="8bd1b-120">El valor de mérito del códec se almacena en el registro para la búsqueda rápida.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="8bd1b-121">La función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ordena los códecs por orden de mérito.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="8bd1b-122">Los códecs con valores de mérito aparecen en la lista detrás de los códecs registrados localmente (consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), pero antes de otros códecs.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="8bd1b-123">Cuando se crea la MFT, el mérito del códec se comprueba mediante la API de [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="8bd1b-124">En el caso de una MFT de proxy, el códec implementa la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="8bd1b-125">En el caso de un controlador AVStream, el códec implementa el \_ conjunto de propiedades OPMVideoOutput de KSPROPSETID.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="8bd1b-126">En el diagrama siguiente se muestra cómo se comprueba el mérito en ambos casos:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-126">The following diagram shows how merit is verified in both cases:</span></span>

![diagrama que muestra dos procesos: uno conduce a través de la MFT del proxy de Media Foundation y el controlador AVStream, el otro a través de la MFT del proxy personalizado](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="8bd1b-128">MFT de proxy personalizado</span><span class="sxs-lookup"><span data-stu-id="8bd1b-128">Custom Proxy MFT</span></span>

<span data-ttu-id="8bd1b-129">Si proporciona un MFT de proxy para el códec de hardware, implemente el valor de mérito del códec como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="8bd1b-130">Implemente la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) en MFT.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="8bd1b-131">El código de ejemplo se muestra en la sección siguiente de este tema.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="8bd1b-132">Agregue el atributo de [ \_ \_ méritos \_ del códec MFT](mft-codec-merit-attribute.md) al registro, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="8bd1b-133">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="8bd1b-134">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para establecer el atributo de [ \_ \_ mérito \_ del códec MFT](mft-codec-merit-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="8bd1b-135">El valor del atributo es el mérito asignado del códec.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="8bd1b-136">Llame a [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) para registrar la MFT.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="8bd1b-137">Pase el almacén de atributos en el parámetro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="8bd1b-138">La aplicación llama a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="8bd1b-139">Esta función devuelve una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , uno para cada códec que coincide con los criterios de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="8bd1b-140">La aplicación llama a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear la MFT.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="8bd1b-141">El método [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) llama a la función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) para comprobar el certificado y el valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="8bd1b-142">La función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) llama a [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) y envía una solicitud de estado de [**\_ \_ \_ información del códec OPM Get**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="8bd1b-143">Esta solicitud de estado devuelve el valor de mérito asignado del códec.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="8bd1b-144">Si este valor no coincide con el valor del registro, puede producirse un error en [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="8bd1b-145">En el código siguiente se muestra cómo agregar el valor de mérito al registro al registrar la MFT:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="8bd1b-146">Implementar IOPMVideoOutput para el mérito del códec</span><span class="sxs-lookup"><span data-stu-id="8bd1b-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="8bd1b-147">En el código siguiente se muestra cómo implementar [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) para el mérito del códec.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="8bd1b-148">Para obtener más información general sobre la API de OPM, consulte [Administrador de protección de salida](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="8bd1b-149">El código que se muestra aquí no tiene ofuscación u otros mecanismos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="8bd1b-150">Está pensada para mostrar la implementación básica del Protocolo de enlace de OPM y la solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="8bd1b-151">En este ejemplo se da por supuesto que *g \_ TestCert* es una matriz de bytes que contiene la cadena de certificados del códec y *g \_ PrivateKey* es una matriz de bytes que contiene la clave privada del certificado:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



<span data-ttu-id="8bd1b-152">En el método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) , genere un número aleatorio para el protocolo de enlace.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="8bd1b-153">Devuelva este número y el certificado al autor de la llamada:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-153">Return this number and the certificate to the caller:</span></span>


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



<span data-ttu-id="8bd1b-154">El método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) completa el protocolo de enlace de OPM:</span><span class="sxs-lookup"><span data-stu-id="8bd1b-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



<span data-ttu-id="8bd1b-155">En el método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) , implemente la solicitud de estado de [**información del \_ \_ códec \_ OPM Get**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="8bd1b-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="8bd1b-156">Los datos de entrada son una estructura de [**\_ parámetros de \_ \_ información \_ de códec OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) que contiene el CLSID de la MFT.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="8bd1b-157">Los datos de salida son una estructura de [**\_ información del códec de obtención de \_ \_ \_ información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) que contiene el mérito del códec.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



<span data-ttu-id="8bd1b-158">El método [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) debe calcular un código de autentificación de mensajes (Mac) (Mac) mediante el algoritmo OMAC-1. consulte [calcular el valor de OMAC-1](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="8bd1b-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="8bd1b-159">No es necesario admitir ninguna otra solicitud de estado de OPM.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="8bd1b-160">Los métodos [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) y [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) no son necesarios para el mérito del códec, por lo que estos métodos pueden devolver **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="8bd1b-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a><span data-ttu-id="8bd1b-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bd1b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd1b-162">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="8bd1b-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="8bd1b-163">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="8bd1b-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 




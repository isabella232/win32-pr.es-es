---
description: Codec Codec Codec (Códec de programación
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Codec Codec Codec (Códec de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065133"
---
# <a name="codec-merit"></a>Codec Codec Codec (Códec de programación

A partir Windows 7, se puede asignar un valor de Media Foundation a un *códec.* Cuando se enumeran los códecs, se prefieren los códecs con mayor puntuación que los códecs con menos afición. Los códecs con cualquier valor de merececión se prefieren a los códecs sin una asignación. Para obtener más información sobre la enumeración de códecs, [**vea MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

Microsoft asigna los valores de los valores de la propiedad. Actualmente, solo los códecs de hardware son aptos para recibir un valor de merececión. Al proveedor de códecs también se le emite un certificado digital, que se usa para comprobar el valor de los valores de los valores del códec. Para obtener un certificado, envíe una solicitud de correo electrónico a wmla@microsoft.com . El proceso para obtener un certificado incluye firmar una licencia y proporcionar un conjunto de archivos de información a Microsoft.

El funcionamiento de los códecs es el siguiente:

1.  El proveedor del códec implementa uno de los siguientes elementos:
    -   Un mini controlador AVStream. Media Foundation proporciona un MFT de proxy estándar para controladores AVStream. Ésta es la opción recomendada.
    -   Una Media Foundation transformación (MFT) que actúa como proxy para el hardware. Para obtener más información, vea [Hardware MFT](hardware-mfts.md).
2.  El valor de valor del códec se almacena en el registro para una búsqueda rápida.
3.  La [**función MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ordena los códecs en orden de conserción. Los códecs con valores de razón aparecen en la lista detrás de códecs registrados localmente (consulte [**MFTRegisterLocal),**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)pero por delante de otros códecs.
4.  Cuando se crea el MFT, el rendimiento del códec se comprueba mediante la API [de Output Protection Manager](output-protection-manager.md) (OPM).
5.  Para un MFT de proxy, el códec implementa la [**interfaz IOPMVideoOutput.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) Para un controlador AVStream, el códec implementa el conjunto de propiedades KSPROPSETID \_ OPMVideoOutput.

En el diagrama siguiente se muestra cómo se comprueba el resultado en ambos casos:

![diagrama que muestra dos procesos: uno conduce a través de media foundation proxy mft y avstream driver, el otro a través de mft de proxy personalizado](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>MFT de proxy personalizado

Si proporciona un MFT de proxy para el códec de hardware, implemente el valor de calidad del códec como se muestra a continuación:

1.  Implemente [**la interfaz IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) en MFT. El código de ejemplo se muestra en la siguiente sección de este tema.
2.  Agregue el [atributo ATTRIBUTE DE CÓDEC \_ \_ DE \_ MFT](mft-codec-merit-attribute.md) al registro, como se muestra a continuación:

    1.  Llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.
    2.  Llame [**aATTRIBUTEAttributes::SetUINT32 para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) establecer el atributo [ATTRIBUTE DE CODEC \_ \_ DE \_ MFT.](mft-codec-merit-attribute.md) El valor del atributo es el atributo asignado del códec.
    3.  Llame [**a MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) para registrar el MFT. Pase el almacén de atributos en el *parámetro pAttributes.*

3.  La aplicación llama [**a MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Esta función devuelve una matriz de punteros [**DE DESACTIVATE,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) una para cada códec que coincida con los criterios de enumeración.
4.  La aplicación llama [**a IMFActivate::ActivateObject para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) crear el MFT.
5.  El [**método ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) llama a [**la función MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) para comprobar el certificado y el valor del premio.
6.  La [**función MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) llama a [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) y envía una solicitud [**de estado \_ OPM GET CODEC \_ \_ INFO.**](opm-get-codec-info.md) Esta solicitud de estado devuelve el valor asignado del códec. Si este valor no coincide con el valor del Registro, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) puede producir un error.

En el código siguiente se muestra cómo agregar el valor de becario al registro al registrar el MFT:


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implementación de IOPMVideoOutput para el códec de prueba

En el código siguiente se muestra cómo implementar [**IOPMVideoOutput para el**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) valor de códec. Para obtener una explicación más general de la API de OPM, consulte [Output Protection Manager](output-protection-manager.md).

> [!Note]  
> El código que se muestra aquí no tiene ofuscación ni otros mecanismos de seguridad. Está diseñado para mostrar la implementación básica del protocolo de enlace OPM y la solicitud de estado.

 

En este ejemplo se supone que *g \_ TestCert* es una matriz de bytes que contiene la cadena de certificados del códec y *g \_ PrivateKey* es una matriz de bytes que contiene la clave privada del certificado:


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



En el [**método IOPMVideoOutput::StartInitialization,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) genere un número aleatorio para el protocolo de enlace. Devuelva este número y el certificado al autor de la llamada:


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



El [**método IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) completa el protocolo de enlace de OPM:


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



En el [**método IOPMVideoOutput::GetInformation,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) implemente la solicitud [**de estado \_ OPM GET CODEC \_ \_ INFO.**](opm-get-codec-info.md) Los datos de entrada son una [**estructura OPM \_ GET CODEC \_ INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) que contiene el CLSID de su MFT. Los datos de salida son una estructura [**OPM \_ GET CODEC INFO \_ \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) que contiene el valor de códec.


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



El [**método GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) debe calcular un código de autenticación de mensajes (MAC) mediante el algoritmo OMAC-1; vea [Cálculo del valor OMAC-1.](opm-example-code.md)

No es necesario admitir ninguna otra solicitud de estado de OPM.

Los métodos [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) y [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) no son necesarios para el acato de códec, por lo que estos métodos pueden devolver **E \_ NOTIMPL**.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Escribir un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 




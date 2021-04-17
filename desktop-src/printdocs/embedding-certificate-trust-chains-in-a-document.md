---
description: En este tema se describe cómo insertar los certificados que componen una cadena de certificados en un documento XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Insertar cadenas de certificado en un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee6476e0c187cf1a62915f0a3ab2b7949586baa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697130"
---
# <a name="embed-certificate-chains-in-a-document"></a>Insertar cadenas de certificado en un documento

En este tema se describe cómo insertar los certificados que componen una cadena de certificados en un documento XPS. Una cadena de certificados consta de todos los certificados, excepto el certificado raíz, que son necesarios para certificar el sujeto identificado por el certificado final.

Para insertar una cadena de certificados en un documento XPS, primero debe crear la cadena de certificados como se muestra en el ejemplo de código siguiente.

El método **CreateCertificateChain** en el ejemplo de código acepta *certificateStore* como parámetro, que es un valor **HCERTSTORE** . Si este valor es **null**, los certificados se recuperarán del servidor de certificados del equipo cliente. Si el valor es el identificador de un almacén de certificados, los certificados se recuperarán de ese almacén al que hacen referencia *certificateStore* y del servidor de certificados del equipo cliente.


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



En el ejemplo de código siguiente se crea una cadena de certificados a partir de certificados y, a continuación, se agregan estos certificados a un documento XPS. Tenga en cuenta que [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) crea la cadena de certificados en la que el certificado de firma es el primero y el certificado raíz es el último. El certificado de firma y el certificado raíz no se agregan en este ejemplo. Los certificados de firma se agregarán con una llamada al método [**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , que debe ser el último método de firma llamado en el documento. El certificado raíz no se agrega cuando el documento está firmado, porque debe ser proporcionado por el servidor de certificados del equipo cliente cuando se valida la firma.


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Comprobar que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Comprobar que el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Se usa en este ejemplo**
</dt> <dt>

[**contexto de certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**CIFRAr \_ información de OID \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[API de criptografía](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Certificados digitales](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Cadenas de certificados](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Comprobación de certificados de confianza](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[Errores de la API de firma digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errores de documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

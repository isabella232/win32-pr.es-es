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
# <a name="embed-certificate-chains-in-a-document"></a><span data-ttu-id="618a5-103">Insertar cadenas de certificado en un documento</span><span class="sxs-lookup"><span data-stu-id="618a5-103">Embed Certificate Chains in a Document</span></span>

<span data-ttu-id="618a5-104">En este tema se describe cómo insertar los certificados que componen una cadena de certificados en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="618a5-104">This topic describes how to embed the certificates that make up a certificate chain into an XPS document.</span></span> <span data-ttu-id="618a5-105">Una cadena de certificados consta de todos los certificados, excepto el certificado raíz, que son necesarios para certificar el sujeto identificado por el certificado final.</span><span class="sxs-lookup"><span data-stu-id="618a5-105">A certificate chain consists of all the certificates, except the root certificate, that are needed to certify the subject identified by the end certificate.</span></span>

<span data-ttu-id="618a5-106">Para insertar una cadena de certificados en un documento XPS, primero debe crear la cadena de certificados como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="618a5-106">To embed a certificate chain into an XPS document, first create the certificate chain as illustrated in the following code example.</span></span>

<span data-ttu-id="618a5-107">El método **CreateCertificateChain** en el ejemplo de código acepta *certificateStore* como parámetro, que es un valor **HCERTSTORE** .</span><span class="sxs-lookup"><span data-stu-id="618a5-107">The **CreateCertificateChain** method in the code example accepts *certificateStore* as a parameter, which is an **HCERTSTORE** value.</span></span> <span data-ttu-id="618a5-108">Si este valor es **null**, los certificados se recuperarán del servidor de certificados del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="618a5-108">If this value is **NULL**, the certificates will be retrieved from the client computer's certificate server.</span></span> <span data-ttu-id="618a5-109">Si el valor es el identificador de un almacén de certificados, los certificados se recuperarán de ese almacén al que hacen referencia *certificateStore* y del servidor de certificados del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="618a5-109">If the value is the handle to a certificate store, the certificates will be retrieved from that store referenced by *certificateStore* as well as from the client computer's certificate server.</span></span>


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



<span data-ttu-id="618a5-110">En el ejemplo de código siguiente se crea una cadena de certificados a partir de certificados y, a continuación, se agregan estos certificados a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="618a5-110">The following code example creates a certificate chain from certificates and then adds these certificates to an XPS document.</span></span> <span data-ttu-id="618a5-111">Tenga en cuenta que [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) crea la cadena de certificados en la que el certificado de firma es el primero y el certificado raíz es el último.</span><span class="sxs-lookup"><span data-stu-id="618a5-111">Note that [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) creates the certificate chain in which the signing certificate is first and the root certificate is last.</span></span> <span data-ttu-id="618a5-112">El certificado de firma y el certificado raíz no se agregan en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="618a5-112">The signing certificate and the root certificate are not added in this example.</span></span> <span data-ttu-id="618a5-113">Los certificados de firma se agregarán con una llamada al método [**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , que debe ser el último método de firma llamado en el documento.</span><span class="sxs-lookup"><span data-stu-id="618a5-113">The signing certificates will be added with a call to the [**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) method, which should be the last signature method called on the document.</span></span> <span data-ttu-id="618a5-114">El certificado raíz no se agrega cuando el documento está firmado, porque debe ser proporcionado por el servidor de certificados del equipo cliente cuando se valida la firma.</span><span class="sxs-lookup"><span data-stu-id="618a5-114">The root certificate is not added when the document is signed, because it must be provided by the client computer's certificate server when the signature is validated.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="618a5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="618a5-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="618a5-116">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="618a5-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="618a5-117">Cargar un certificado desde un archivo</span><span class="sxs-lookup"><span data-stu-id="618a5-117">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="618a5-118">Comprobar que un certificado admite un método de firma</span><span class="sxs-lookup"><span data-stu-id="618a5-118">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="618a5-119">Comprobar que el sistema admite un método de síntesis</span><span class="sxs-lookup"><span data-stu-id="618a5-119">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

<span data-ttu-id="618a5-120">**Se usa en este ejemplo**</span><span class="sxs-lookup"><span data-stu-id="618a5-120">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="618a5-121">**contexto de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="618a5-121">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="618a5-122">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="618a5-122">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="618a5-123">**CIFRAr \_ información de OID \_**</span><span class="sxs-lookup"><span data-stu-id="618a5-123">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[<span data-ttu-id="618a5-124">**IOpcCertificateSet**</span><span class="sxs-lookup"><span data-stu-id="618a5-124">**IOpcCertificateSet**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[<span data-ttu-id="618a5-125">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="618a5-125">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

<span data-ttu-id="618a5-126">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="618a5-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="618a5-127">API de criptografía</span><span class="sxs-lookup"><span data-stu-id="618a5-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="618a5-128">Funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="618a5-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="618a5-129">Certificados digitales</span><span class="sxs-lookup"><span data-stu-id="618a5-129">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[<span data-ttu-id="618a5-130">Cadenas de certificados</span><span class="sxs-lookup"><span data-stu-id="618a5-130">Certificate Chains</span></span>](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[<span data-ttu-id="618a5-131">Comprobación de certificados de confianza</span><span class="sxs-lookup"><span data-stu-id="618a5-131">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[<span data-ttu-id="618a5-132">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="618a5-132">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="618a5-133">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="618a5-133">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="618a5-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="618a5-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

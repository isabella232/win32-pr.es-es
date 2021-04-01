---
description: En este tema se describe cómo firmar un documento XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Firmar un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909365"
---
# <a name="sign-a-document"></a><span data-ttu-id="5ed62-103">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="5ed62-103">Sign a Document</span></span>

<span data-ttu-id="5ed62-104">En este tema se describe cómo firmar un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5ed62-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="5ed62-105">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="5ed62-106">Para firmar un documento XPS, cárguelo primero en un administrador de firmas como se describe en [inicializar el administrador de firmas](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="5ed62-107">Para firmar un documento que se ha cargado en un administrador de firmas:</span><span class="sxs-lookup"><span data-stu-id="5ed62-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="5ed62-108">Cree una instancia de una interfaz [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .</span><span class="sxs-lookup"><span data-stu-id="5ed62-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="5ed62-109">Establezca la Directiva de firma.</span><span class="sxs-lookup"><span data-stu-id="5ed62-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="5ed62-110">Establezca el método Signature.</span><span class="sxs-lookup"><span data-stu-id="5ed62-110">Set the signature method.</span></span> <span data-ttu-id="5ed62-111">Las constantes de cadena URI del método de firma se definen en cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="5ed62-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="5ed62-112">Para obtener más información sobre los valores válidos de los métodos de firma, vea [**IXpsSigningOptions:: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="5ed62-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="5ed62-113">Establezca el método de síntesis.</span><span class="sxs-lookup"><span data-stu-id="5ed62-113">Set the digest method.</span></span> <span data-ttu-id="5ed62-114">Las constantes de cadena URI del método de síntesis se definen en cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="5ed62-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="5ed62-115">Para obtener información sobre los valores de método de síntesis válidos, vea [**IXpsSigningOptions:: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="5ed62-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="5ed62-116">Cargue el certificado como se describe en [carga de un certificado desde un archivo](load-a-certificate-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="5ed62-117">Compruebe que el certificado admite el método de firma, tal como se describe en [comprobación de que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="5ed62-118">Compruebe que el sistema admite el método de síntesis, tal como se describe en comprobación de que [el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="5ed62-119">Si es necesario, inserte los certificados de la cadena de confianza de certificados en el documento XPS tal y como se describe en [Insertar cadenas de certificados en un documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="5ed62-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="5ed62-120">Firme el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5ed62-120">Sign the XPS document.</span></span>

<span data-ttu-id="5ed62-121">En el ejemplo de código siguiente se muestra cómo usar los pasos anteriores en un programa.</span><span class="sxs-lookup"><span data-stu-id="5ed62-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a><span data-ttu-id="5ed62-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed62-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5ed62-123">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="5ed62-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5ed62-124">Agregar una solicitud de firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="5ed62-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="5ed62-125">Comprobar las firmas del documento</span><span class="sxs-lookup"><span data-stu-id="5ed62-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="5ed62-126">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="5ed62-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="5ed62-127">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="5ed62-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="5ed62-128">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="5ed62-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="5ed62-129">**IXpsSignatureManager::CreateSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="5ed62-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="5ed62-130">**IXpsSignatureManager:: Sign**</span><span class="sxs-lookup"><span data-stu-id="5ed62-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="5ed62-131">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="5ed62-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="5ed62-132">**IXpsSigningOptions::SetDigestMethod**</span><span class="sxs-lookup"><span data-stu-id="5ed62-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="5ed62-133">**IXpsSigningOptions::SetPolicy**</span><span class="sxs-lookup"><span data-stu-id="5ed62-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="5ed62-134">**IXpsSigningOptions::SetSignatureMethod**</span><span class="sxs-lookup"><span data-stu-id="5ed62-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="5ed62-135">**\_Directiva de firma de XPS \_**</span><span class="sxs-lookup"><span data-stu-id="5ed62-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="5ed62-136">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="5ed62-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5ed62-137">API de criptografía</span><span class="sxs-lookup"><span data-stu-id="5ed62-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="5ed62-138">Funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="5ed62-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="5ed62-139">Cargar un certificado desde un archivo</span><span class="sxs-lookup"><span data-stu-id="5ed62-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="5ed62-140">Comprobar que un certificado admite un método de firma</span><span class="sxs-lookup"><span data-stu-id="5ed62-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="5ed62-141">Comprobar que el sistema admite un método de síntesis</span><span class="sxs-lookup"><span data-stu-id="5ed62-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="5ed62-142">Insertar cadenas de certificado en un documento</span><span class="sxs-lookup"><span data-stu-id="5ed62-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="5ed62-143">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="5ed62-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="5ed62-144">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="5ed62-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="5ed62-145">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5ed62-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

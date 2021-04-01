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
# <a name="sign-a-document"></a>Firmar un documento

En este tema se describe cómo firmar un documento XPS.

Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).

Para firmar un documento XPS, cárguelo primero en un administrador de firmas como se describe en [inicializar el administrador de firmas](initialize-the-signature-manager.md).

Para firmar un documento que se ha cargado en un administrador de firmas:

1.  Cree una instancia de una interfaz [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .
2.  Establezca la Directiva de firma.
3.  Establezca el método Signature. Las constantes de cadena URI del método de firma se definen en cryptxml. h. Para obtener más información sobre los valores válidos de los métodos de firma, vea [**IXpsSigningOptions:: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Establezca el método de síntesis. Las constantes de cadena URI del método de síntesis se definen en cryptxml. h. Para obtener información sobre los valores de método de síntesis válidos, vea [**IXpsSigningOptions:: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Cargue el certificado como se describe en [carga de un certificado desde un archivo](load-a-certificate-from-a-file.md).
6.  Compruebe que el certificado admite el método de firma, tal como se describe en [comprobación de que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md).
7.  Compruebe que el sistema admite el método de síntesis, tal como se describe en comprobación de que [el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md).
8.  Si es necesario, inserte los certificados de la cadena de confianza de certificados en el documento XPS tal y como se describe en [Insertar cadenas de certificados en un documento](embedding-certificate-trust-chains-in-a-document.md).
9.  Firme el documento XPS.

En el ejemplo de código siguiente se muestra cómo usar los pasos anteriores en un programa.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Agregar una solicitud de firma a un documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Comprobar las firmas del documento](verify-document-signatures.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::CreateSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions::SetPolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**\_Directiva de firma de XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[API de criptografía](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funciones de criptografía](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)
</dt> <dt>

[Comprobar que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Comprobar que el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Insertar cadenas de certificado en un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Errores de la API de firma digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errores de documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

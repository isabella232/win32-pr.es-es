---
description: En este tema se enumeran las consideraciones para usar la API de firma digital XPS para agregar firmas digitales a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso de la API de firma digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909573"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="e0e26-103">Uso de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="e0e26-104">En este tema se enumeran las consideraciones para usar la API de firma digital XPS para agregar firmas digitales a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="e0e26-105">La API de firma digital XPS permite a las aplicaciones solicitar a los usuarios que firmen documentos XPS y comprobar las firmas que se encuentran en los documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="e0e26-106">La API de firma digital XPS se puede aplicar a un documento XPS sin cargarlo en un OM XPS y se puede usar en flujos de documento XPS que se serializan desde un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="e0e26-107">La sección tareas de programación de la [API de firma digital XPS](#xps-digital-signature-api-programming-tasks) contiene temas que describen cómo programar con la API de firma digital XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="e0e26-108">En este tema se enumeran las siguientes consideraciones sobre el uso de la API de firma digital XPS al agregar compatibilidad con firmas digitales a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0e26-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="e0e26-109">Tareas de programación de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="e0e26-110">Notas especiales sobre la programación de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="e0e26-111">Comprobar las firmas digitales en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="e0e26-112">Directiva de firma de firma digital</span><span class="sxs-lookup"><span data-stu-id="e0e26-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="e0e26-113">Incrustar una cadena de certificados</span><span class="sxs-lookup"><span data-stu-id="e0e26-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="e0e26-114">Usar la \_ estructura de contexto CERT</span><span class="sxs-lookup"><span data-stu-id="e0e26-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="e0e26-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0e26-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="e0e26-116">Tareas de programación de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="e0e26-117">Esta sección contiene temas que describen cómo realizar tareas de programación con la API de firma digital XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="e0e26-118">Tareas comunes de programación de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="e0e26-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="e0e26-119">Inicializar el administrador de firmas</span><span class="sxs-lookup"><span data-stu-id="e0e26-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="e0e26-120">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="e0e26-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="e0e26-121">Agregar una solicitud de firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="e0e26-122">Comprobar las firmas del documento</span><span class="sxs-lookup"><span data-stu-id="e0e26-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="e0e26-123">Tareas adicionales de programación de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="e0e26-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="e0e26-124">Cargar un certificado desde un archivo</span><span class="sxs-lookup"><span data-stu-id="e0e26-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="e0e26-125">Comprobar que un certificado admite un método de firma</span><span class="sxs-lookup"><span data-stu-id="e0e26-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="e0e26-126">Comprobar que el sistema admite un método de síntesis</span><span class="sxs-lookup"><span data-stu-id="e0e26-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="e0e26-127">Insertar cadenas de certificado en un documento</span><span class="sxs-lookup"><span data-stu-id="e0e26-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="e0e26-128">Notas especiales sobre la programación de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="e0e26-129">Los temas siguientes requieren una consideración especial al usar la API de firma digital XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="e0e26-130">Comprobar las firmas digitales en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="e0e26-131">Directiva de firma de firma digital</span><span class="sxs-lookup"><span data-stu-id="e0e26-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="e0e26-132">Incrustar una cadena de certificados</span><span class="sxs-lookup"><span data-stu-id="e0e26-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="e0e26-133">Usar la \_ estructura de contexto CERT</span><span class="sxs-lookup"><span data-stu-id="e0e26-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="e0e26-134">Comprobar las firmas digitales en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="e0e26-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="e0e26-135">[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) comprueba solo el contenido firmado para determinar que no ha cambiado desde que se firmó.</span><span class="sxs-lookup"><span data-stu-id="e0e26-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="e0e26-136">**IXpsSignature:: Verify** no comprueba ninguno de los certificados que se usaron para firmar el contenido del documento.</span><span class="sxs-lookup"><span data-stu-id="e0e26-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="e0e26-137">Para obtener más información acerca de los certificados y la criptografía, consulte [acerca de la criptografía](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="e0e26-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="e0e26-138">Para ver un ejemplo de cómo comprobar las firmas de documento en un programa, consulte [comprobación de firmas y certificados de documento](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e0e26-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="e0e26-139">Directiva de firma de firma digital</span><span class="sxs-lookup"><span data-stu-id="e0e26-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="e0e26-140">La Directiva de firma de firmas digitales determina qué partes de un documento XPS están firmadas.</span><span class="sxs-lookup"><span data-stu-id="e0e26-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="e0e26-141">Una opción de directiva de firma es firmar las relaciones de firma que se inician desde la parte del origen de la firma.</span><span class="sxs-lookup"><span data-stu-id="e0e26-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="e0e26-142">Dado que las relaciones de firma cambian con cada firma que se agrega, las firmas que se realicen en esta Directiva se interrumpirán cuando se agreguen nuevas firmas.</span><span class="sxs-lookup"><span data-stu-id="e0e26-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="e0e26-143">Asegúrese de que comprende claramente las implicaciones y los efectos de la configuración de esta Directiva; de lo contrario, podría producirse un comportamiento inesperado o no deseado.</span><span class="sxs-lookup"><span data-stu-id="e0e26-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="e0e26-144">Para obtener más información acerca de las directivas de firma, consulte [**\_ \_ Directiva**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)de firma de XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="e0e26-145">Incrustar una cadena de certificados</span><span class="sxs-lookup"><span data-stu-id="e0e26-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="e0e26-146">Los certificados que componen la cadena de confianza de un certificado específico se pueden agregar a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="e0e26-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="e0e26-147">La inserción de estos certificados puede facilitar, en escenarios sin conexión, que una aplicación Compruebe los certificados que usa una firma digital.</span><span class="sxs-lookup"><span data-stu-id="e0e26-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="e0e26-148">Para obtener más información sobre cómo insertar certificados en un documento XPS, consulte [Insertar cadenas de certificados en un documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="e0e26-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="e0e26-149">Usar la \_ estructura de contexto CERT</span><span class="sxs-lookup"><span data-stu-id="e0e26-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="e0e26-150">Las estructuras de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado y de [**\_ información de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) son las estructuras de datos principales que contienen información de certificado.</span><span class="sxs-lookup"><span data-stu-id="e0e26-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="e0e26-151">Para obtener más información sobre el uso de estas estructuras, vea [usar una \_ estructura de datos de información de certificado](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="e0e26-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="e0e26-152">[**Certificado \_ de**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Las estructuras de contexto devueltas por las funciones de Crypto API deben liberarse cuando ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="e0e26-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="e0e26-153">Para liberar una estructura de **\_ contexto de certificado** , llame a la función [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="e0e26-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0e26-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0e26-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0e26-155">Tareas comunes de programación de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="e0e26-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="e0e26-156">Tareas adicionales de programación de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="e0e26-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="e0e26-157">**contexto de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="e0e26-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="e0e26-158">**información de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="e0e26-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="e0e26-159">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="e0e26-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="e0e26-160">**\_Directiva de firma de XPS \_**</span><span class="sxs-lookup"><span data-stu-id="e0e26-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="e0e26-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e0e26-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

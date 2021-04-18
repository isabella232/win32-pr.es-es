---
description: PKCS \# 7 es un estándar de sintaxis de mensajes criptográficos.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#Atributos PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688260"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="e5000-103">\#Atributos PKCS 7</span><span class="sxs-lookup"><span data-stu-id="e5000-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="e5000-104">PKCS \# 7 es un estándar de sintaxis de mensajes criptográficos.</span><span class="sxs-lookup"><span data-stu-id="e5000-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="e5000-105">Un \# mensaje PKCS 7 no constituye una solicitud de certificado, sino que puede encapsular una \# solicitud PKCS 10 o CMC en una estructura **ContentInfo** ASN. 1 mediante el uso de uno de los siguientes tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="e5000-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="e5000-106">La encapsulación permite agregar funcionalidad adicional, como varias firmas, que no está disponible de otro modo.</span><span class="sxs-lookup"><span data-stu-id="e5000-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="e5000-107">**Data**</span><span class="sxs-lookup"><span data-stu-id="e5000-107">**Data**</span></span>
-   <span data-ttu-id="e5000-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="e5000-108">**SignedData**</span></span>
-   <span data-ttu-id="e5000-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="e5000-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="e5000-110">**SignedAndEnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="e5000-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="e5000-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="e5000-111">**DigestedData**</span></span>
-   <span data-ttu-id="e5000-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="e5000-112">**EncryptedData**</span></span>

<span data-ttu-id="e5000-113">Los atributos se pueden agregar a los campos **authenticatedAttributes** y **unauthenticatedAttributes** del tipo de contenido **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="e5000-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="e5000-114">El proceso necesario para archivar la clave privada de un cliente en una entidad de certificación (CA) proporciona un ejemplo completo de cómo se pueden usar los atributos autenticados (firmados) y los atributos no autenticados:</span><span class="sxs-lookup"><span data-stu-id="e5000-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="e5000-115">El cliente crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y agrega los datos adecuados para el tipo de certificado que se solicita.</span><span class="sxs-lookup"><span data-stu-id="e5000-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="e5000-116">El cliente usa la \# solicitud PKCS 10 para inicializar un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="e5000-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="e5000-117">La \# solicitud PKCS 10 se coloca en la estructura **TaggedRequest** de la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="e5000-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="e5000-118">Para obtener más información, consulte [atributos de CMC](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e5000-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="e5000-119">El cliente cifra una clave privada y la usa para inicializar un objeto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) .</span><span class="sxs-lookup"><span data-stu-id="e5000-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="e5000-120">El nuevo atributo **ArchiveKey** se encapsula en una estructura **EnvelopedData** .</span><span class="sxs-lookup"><span data-stu-id="e5000-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   <span data-ttu-id="e5000-121">El cliente crea un hash SHA-1 de la clave cifrada y lo utiliza para inicializar un objeto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .</span><span class="sxs-lookup"><span data-stu-id="e5000-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="e5000-122">El cliente recupera la colección [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) de la solicitud CMC y le agrega los atributos **ArchiveKey** y **ArchiveKeyHash** .</span><span class="sxs-lookup"><span data-stu-id="e5000-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="e5000-123">Los atributos se colocan en la estructura **TaggedAttributes** de la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="e5000-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="e5000-124">El cliente usa la solicitud CMC para inicializar un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) .</span><span class="sxs-lookup"><span data-stu-id="e5000-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="e5000-125">Esto coloca la solicitud CMC en el campo **contentInfo** de la \# estructura PKCS 7 **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="e5000-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="e5000-126">El atributo **ArchiveKeyHash** está firmado y colocado en la secuencia **authenticatedAttributes** de la estructura **SignerInfo** .</span><span class="sxs-lookup"><span data-stu-id="e5000-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="e5000-127">El atributo **ArchiveKey** se coloca en la secuencia **unauthenticatedAttributes** de la estructura **SignerInfo** asociada al firmante principal del mensaje PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="e5000-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5000-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5000-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5000-129">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="e5000-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 




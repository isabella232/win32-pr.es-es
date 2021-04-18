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
# <a name="pkcs-7-attributes"></a>\#Atributos PKCS 7

PKCS \# 7 es un estándar de sintaxis de mensajes criptográficos. Un \# mensaje PKCS 7 no constituye una solicitud de certificado, sino que puede encapsular una \# solicitud PKCS 10 o CMC en una estructura **ContentInfo** ASN. 1 mediante el uso de uno de los siguientes tipos de contenido. La encapsulación permite agregar funcionalidad adicional, como varias firmas, que no está disponible de otro modo.

-   **Data**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **EncryptedData**

Los atributos se pueden agregar a los campos **authenticatedAttributes** y **unauthenticatedAttributes** del tipo de contenido **SignedData** .

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

El proceso necesario para archivar la clave privada de un cliente en una entidad de certificación (CA) proporciona un ejemplo completo de cómo se pueden usar los atributos autenticados (firmados) y los atributos no autenticados:

-   El cliente crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y agrega los datos adecuados para el tipo de certificado que se solicita.
-   El cliente usa la \# solicitud PKCS 10 para inicializar un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . La \# solicitud PKCS 10 se coloca en la estructura **TaggedRequest** de la solicitud CMC. Para obtener más información, consulte [atributos de CMC](cmc-attributes.md).
-   El cliente cifra una clave privada y la usa para inicializar un objeto [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) . El nuevo atributo **ArchiveKey** se encapsula en una estructura **EnvelopedData** .

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

-   El cliente crea un hash SHA-1 de la clave cifrada y lo utiliza para inicializar un objeto [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .
-   El cliente recupera la colección [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) de la solicitud CMC y le agrega los atributos **ArchiveKey** y **ArchiveKeyHash** . Los atributos se colocan en la estructura **TaggedAttributes** de la solicitud CMC.
-   El cliente usa la solicitud CMC para inicializar un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) . Esto coloca la solicitud CMC en el campo **contentInfo** de la \# estructura PKCS 7 **SignedData** .
-   El atributo **ArchiveKeyHash** está firmado y colocado en la secuencia **authenticatedAttributes** de la estructura **SignerInfo** .
-   El atributo **ArchiveKey** se coloca en la secuencia **unauthenticatedAttributes** de la estructura **SignerInfo** asociada al firmante principal del mensaje PKCS \# 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos compatibles](supported-attributes.md)
</dt> </dl>

 

 




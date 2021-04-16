---
description: La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar contenido.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificados de clave pública X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571249"
---
# <a name="x509-public-key-certificates"></a><span data-ttu-id="2b8e8-103">Certificados de clave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="2b8e8-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="2b8e8-104">La criptografía de clave pública se basa en un par de claves pública y privada para cifrar y descifrar contenido.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="2b8e8-105">Las claves están relacionadas matemáticamente y el contenido cifrado mediante una de las claves solo se puede descifrar con el otro.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="2b8e8-106">La clave privada se mantiene en secreto.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-106">The private key is kept secret.</span></span> <span data-ttu-id="2b8e8-107">Normalmente, la clave pública se incrusta en un certificado binario y el certificado se publica en una base de datos a la que pueden tener acceso todos los usuarios autorizados.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="2b8e8-108">La norma de infraestructura de clave pública (PKI) X. 509 identifica los requisitos de los certificados de clave pública sólidos.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="2b8e8-109">Un certificado es una estructura de datos firmada que enlaza una clave pública a una persona, un equipo o una organización.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="2b8e8-110">Los certificados los emiten [*las entidades de certificación*](/windows/desktop/SecGloss/c-gly) (CA).</span><span class="sxs-lookup"><span data-stu-id="2b8e8-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="2b8e8-111">Todos los usuarios que son parte de la seguridad de las comunicaciones que hacen uso de una clave pública dependen de la entidad de certificación para comprobar adecuadamente las identidades de los usuarios, sistemas o entidades a los que emite certificados.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="2b8e8-112">El nivel de comprobación suele depender del nivel de seguridad necesario para la transacción.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="2b8e8-113">Si la entidad de certificación puede comprobar la identidad del solicitante, firma (cifra), codifica y emite el certificado.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="2b8e8-114">Un certificado es una estructura de datos firmada que enlaza una clave pública a una entidad.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="2b8e8-115">En el ejemplo siguiente se muestra la sintaxis de la [*notación de sintaxis abstracta uno*](/windows/desktop/SecGloss/a-gly) (ASN. 1) para el certificado de versión 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) .</span><span class="sxs-lookup"><span data-stu-id="2b8e8-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

<span data-ttu-id="2b8e8-116">Desde su inicio en 1998, han evolucionado tres versiones del estándar de certificados de clave pública X. 509.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="2b8e8-117">Tal y como se muestra en la siguiente ilustración, cada versión sucesiva de la estructura de datos ha retenido los campos que existían en las versiones anteriores y ha agregado más.</span><span class="sxs-lookup"><span data-stu-id="2b8e8-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![certificados x. 509 versiones 1, 2 y 3](images/x509certificateversions.png)

<span data-ttu-id="2b8e8-119">En los temas siguientes se describen los campos disponibles con más detalle:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="2b8e8-120">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="2b8e8-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="2b8e8-121">Campos de la versión 2</span><span class="sxs-lookup"><span data-stu-id="2b8e8-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="2b8e8-122">Extensiones de la versión 3</span><span class="sxs-lookup"><span data-stu-id="2b8e8-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="2b8e8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b8e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b8e8-124">Infraestructura de clave pública</span><span class="sxs-lookup"><span data-stu-id="2b8e8-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 

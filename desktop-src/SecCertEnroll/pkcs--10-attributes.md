---
description: Los atributos se incluyen en una \# solicitud de certificado PKCS 10 agregándolas a la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis ASN. 1.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Atributos PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361636"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="dce38-103">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="dce38-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="dce38-104">Los atributos se incluyen en una \# solicitud de certificado PKCS 10 agregándolas a la estructura **CertificationRequestInfo** que se muestra en el siguiente ejemplo de sintaxis ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="dce38-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="dce38-105">Para obtener más información sobre cómo puede agregar atributos a una solicitud, vea el tema sobre la [arquitectura de atributo](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="dce38-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="dce38-106">El atributo que se agrega normalmente a una \# solicitud PKCS 10 es una colección de extensiones de la versión 3 definida por un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="dce38-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="dce38-107">Dado que una \# solicitud PKCS 10 no contiene un campo al que se puedan agregar las extensiones directamente, deben agregarse como atributo.</span><span class="sxs-lookup"><span data-stu-id="dce38-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="dce38-108">Los atributos **ClientID**, **CspProvider**, **OSVersion** y **RenewalCertificate** también se pueden agregar a un archivo PKCS).</span><span class="sxs-lookup"><span data-stu-id="dce38-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dce38-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dce38-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dce38-110">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="dce38-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 




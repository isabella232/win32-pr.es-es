---
description: Las extensiones se incluyen en una \# solicitud de certificado PKCS 10 agregándolas al campo atributos de la estructura CertificationRequestInfo que se muestra en el siguiente ejemplo de sintaxis ASN. 1. Para obtener más información, vea el tema atributos.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Extensiones PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669900"
---
# <a name="pkcs-10-extensions"></a><span data-ttu-id="e763f-104">\#Extensiones PKCS 10</span><span class="sxs-lookup"><span data-stu-id="e763f-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="e763f-105">Las extensiones se incluyen en una \# solicitud de certificado PKCS 10 agregándolas al campo **atributos** de la estructura **CertificationRequestInfo** que se muestra en el siguiente ejemplo de sintaxis ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="e763f-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="e763f-106">Para obtener más información, vea el tema [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="e763f-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="e763f-107">En el procedimiento siguiente se describe cómo usar la API de inscripción de certificados para agregar extensiones a una \# solicitud de certificado PKCS 10:</span><span class="sxs-lookup"><span data-stu-id="e763f-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="e763f-108">Recupere una colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) llamando a la propiedad [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) en el objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="e763f-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="e763f-109">Cree una extensión mediante cualquiera de las interfaces disponibles que derivan de la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="e763f-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="e763f-110">Agregue las extensiones creadas en el paso 2 a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="e763f-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e763f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e763f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e763f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e763f-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="e763f-113">Arquitectura de atributo</span><span class="sxs-lookup"><span data-stu-id="e763f-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="e763f-114">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="e763f-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="e763f-115">Extensiones</span><span class="sxs-lookup"><span data-stu-id="e763f-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 




---
description: Las extensiones se incluyen en una solicitud CMC agregándolas a la estructura TaggedAttributes que se muestra en el siguiente ejemplo de sintaxis ASN. 1. Para obtener más información, vea el tema atributos.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensiones de CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277963"
---
# <a name="cmc-extensions"></a><span data-ttu-id="d3c06-104">Extensiones de CMC</span><span class="sxs-lookup"><span data-stu-id="d3c06-104">CMC Extensions</span></span>

<span data-ttu-id="d3c06-105">Las extensiones se incluyen en una solicitud CMC agregándolas a la estructura **TaggedAttributes** que se muestra en el siguiente ejemplo de sintaxis ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="d3c06-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="d3c06-106">Para obtener más información, vea el tema [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="d3c06-107">Cada estructura de la colección **TaggedAttributes** contiene un identificador entero, un identificador de objeto ASN. 1 (OID) y un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="d3c06-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="d3c06-108">Las extensiones se incorporan en una solicitud agregando una estructura **CmcAddExtensions** al campo **valores** .</span><span class="sxs-lookup"><span data-stu-id="d3c06-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="d3c06-109">En el ejemplo siguiente se muestra la sintaxis de la estructura ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="d3c06-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="d3c06-110">El identificador de objeto es **XCN \_ OID \_ CMC \_ Add \_ extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="d3c06-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

<span data-ttu-id="d3c06-111">En el procedimiento siguiente se describe cómo usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado CMC.</span><span class="sxs-lookup"><span data-stu-id="d3c06-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="d3c06-112">**Para usar la API de inscripción de certificados para agregar extensiones a una solicitud de certificado CMC**</span><span class="sxs-lookup"><span data-stu-id="d3c06-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="d3c06-113">Cree una extensión mediante cualquiera de las interfaces disponibles que derivan de la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) o use el objeto **IX509Extension** directamente para crear extensiones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d3c06-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="d3c06-114">Llame a la propiedad [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) del objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para recuperar una colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="d3c06-115">Agregue las extensiones creadas en el paso 1 a la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="d3c06-116">Llame a [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para realizar automáticamente las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="d3c06-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="d3c06-117">Recupere un objeto [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) del objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="d3c06-118">Cree e inicialice un objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) mediante la colección [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) recuperada en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="d3c06-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="d3c06-119">Cree una colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) y agréguele el objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="d3c06-120">Use la colección [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) para inicializar un objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="d3c06-121">Agregue el objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) a la colección [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="d3c06-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c06-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3c06-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c06-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3c06-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="d3c06-124">Arquitectura de atributo</span><span class="sxs-lookup"><span data-stu-id="d3c06-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="d3c06-125">Atributos de CMC</span><span class="sxs-lookup"><span data-stu-id="d3c06-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3c06-126">Extensiones</span><span class="sxs-lookup"><span data-stu-id="d3c06-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 




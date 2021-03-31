---
description: En la práctica, la estructura de una solicitud CMC, que se muestra con la sintaxis siguiente, es relativamente compleja, ya que a menudo contiene solicitudes anidadas.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Atributos de CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815787"
---
# <a name="cmc-attributes"></a><span data-ttu-id="698d6-103">Atributos de CMC</span><span class="sxs-lookup"><span data-stu-id="698d6-103">CMC Attributes</span></span>

<span data-ttu-id="698d6-104">En la práctica, la estructura de una solicitud CMC, que se muestra con la sintaxis siguiente, es relativamente compleja, ya que a menudo contiene solicitudes anidadas.</span><span class="sxs-lookup"><span data-stu-id="698d6-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="698d6-105">Por ejemplo, una solicitud CMC puede contener cero o una solicitud PKCS \# 10 en una secuencia **TaggedRequest** , y puede contener cero o un mensaje PKCS \# 7 en una secuencia **TaggedContentInfo** .</span><span class="sxs-lookup"><span data-stu-id="698d6-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="698d6-106">Cada mensaje PKCS 7 anidado \# puede contener una solicitud CMC que, a su vez, puede contener más solicitudes.</span><span class="sxs-lookup"><span data-stu-id="698d6-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="698d6-107">El número de niveles de anidamiento es teóricamente ilimitado, pero la entidad de certificación (CA) se configura normalmente para limitar el tamaño de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="698d6-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="698d6-108">Los atributos se pueden aplicar a la solicitud de nivel superior o a las solicitudes anidadas.</span><span class="sxs-lookup"><span data-stu-id="698d6-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="698d6-109">Esto se describe en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="698d6-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="698d6-110">Estructura CMCData</span><span class="sxs-lookup"><span data-stu-id="698d6-110">CMCData Structure</span></span>

<span data-ttu-id="698d6-111">Una solicitud CMC contiene secuencias de estructuras **TaggedAttribute**, **TaggedRequest** y **TaggedContentInfo** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="698d6-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a><span data-ttu-id="698d6-112">Estructura TaggedAttribute</span><span class="sxs-lookup"><span data-stu-id="698d6-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="698d6-113">Los atributos se incluyen en una solicitud de certificado CMC agregándolas a la colección **TaggedAttribute** .</span><span class="sxs-lookup"><span data-stu-id="698d6-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="698d6-114">Cada estructura de la colección contiene un identificador entero, un identificador de objeto ASN. 1 (OID) y un conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="698d6-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="698d6-115">Los valores posibles pueden ser cualquiera de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="698d6-115">The possible values can be any of the following.</span></span>

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a><span data-ttu-id="698d6-116">CMCAddAttributes</span><span class="sxs-lookup"><span data-stu-id="698d6-116">CMCAddAttributes</span></span>

<span data-ttu-id="698d6-117">Si los atributos de esta estructura se aplican a una solicitud anidada PKCS \# 10, el campo **certReferences** contendrá el **BodyPartID** que identifica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="698d6-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="698d6-118">Si los atributos se aplican a una solicitud CMC anidada, el campo **pkiDataReference** contendrá el **BodyPartID** de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="698d6-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="698d6-119">Actualmente, solo uno de estos campos puede ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="698d6-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="698d6-120">Los atributos que se pueden incluir se enumeran en el tema [atributos admitidos](supported-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="698d6-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="698d6-121">CmcAddExtensions</span><span class="sxs-lookup"><span data-stu-id="698d6-121">CmcAddExtensions</span></span>

<span data-ttu-id="698d6-122">Esta estructura puede contener extensiones X. 509 versión 3 más extensiones definidas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="698d6-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="698d6-123">Este atributo se define mediante la interfaz [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="698d6-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="698d6-124">Si las extensiones se aplican a una solicitud PKCS 10 anidada \# , el campo **certReferences** contendrá el **BodyPartID** que identifica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="698d6-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="698d6-125">Si las extensiones se aplican a una solicitud CMC anidada, el campo **pkiDataReference** contendrá el **BodyPartID** de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="698d6-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="698d6-126">Actualmente, solo uno de estos campos puede ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="698d6-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="698d6-127">SenderNonce</span><span class="sxs-lookup"><span data-stu-id="698d6-127">SenderNonce</span></span>

<span data-ttu-id="698d6-128">Un nonce son datos binarios aleatorios o pseudoaleatorios que se pueden incluir en una solicitud de certificado y una transacción de respuesta para garantizar que la respuesta o la solicitud no es una repetición de un mensaje anterior.</span><span class="sxs-lookup"><span data-stu-id="698d6-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="698d6-129">Para obtener más información, vea la propiedad [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .</span><span class="sxs-lookup"><span data-stu-id="698d6-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="698d6-130">Transpuestos</span><span class="sxs-lookup"><span data-stu-id="698d6-130">TransactID</span></span>

<span data-ttu-id="698d6-131">Se puede realizar un seguimiento de una solicitud de certificado de ida y vuelta y una transacción de respuesta mediante un identificador.</span><span class="sxs-lookup"><span data-stu-id="698d6-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="698d6-132">El cliente genera un identificador de transacción y lo conserva hasta que el certificado o la entidad de registro responde con un mensaje que completa la transacción.</span><span class="sxs-lookup"><span data-stu-id="698d6-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="698d6-133">La respuesta incluye el identificador.</span><span class="sxs-lookup"><span data-stu-id="698d6-133">The response includes the identifier.</span></span> <span data-ttu-id="698d6-134">Para obtener más información, vea la propiedad [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .</span><span class="sxs-lookup"><span data-stu-id="698d6-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="698d6-135">RegInfo</span><span class="sxs-lookup"><span data-stu-id="698d6-135">RegInfo</span></span>

<span data-ttu-id="698d6-136">Este atributo se puede usar para contener cualquier información de registro que el cliente decida incluir en la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="698d6-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="698d6-137">El valor del atributo es una cadena que contiene pares de nombre y valor concatenados.</span><span class="sxs-lookup"><span data-stu-id="698d6-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="698d6-138">Para obtener más información, vea la propiedad [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="698d6-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="698d6-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="698d6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="698d6-140">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="698d6-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 




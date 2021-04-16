---
description: El concepto de un tipo de datos es fundamental para el estándar de notación de sintaxis abstracta uno (ASN. 1).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema de tipos ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669908"
---
# <a name="asn1-type-system"></a><span data-ttu-id="4bfb7-103">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4bfb7-103">ASN.1 Type System</span></span>

<span data-ttu-id="4bfb7-104">El concepto de un tipo de datos es fundamental para el estándar de notación de sintaxis abstracta uno (ASN. 1).</span><span class="sxs-lookup"><span data-stu-id="4bfb7-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="4bfb7-105">Cada campo de una estructura de solicitud de certificado está asociado a un tipo.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="4bfb7-106">Considere, por ejemplo, la \# Sintaxis de certificado PKCS 10 ASN. 1 que se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="4bfb7-107">La estructura de solicitud de alto nivel, **CertificationRequestInfo**, es un tipo que se compone de una secuencia de otros tipos.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="4bfb7-108">Cuando un tipo es o contiene solo tipos básicos, tipos de cadena o **cualquiera**, no se puede desglosar más.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="4bfb7-109">Por ejemplo, el campo **version** es un tipo **CertificationRequestInfoVersion** que, a su vez, es un tipo **entero** , un tipo ASN. 1 básico que no se compone de otros tipos.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="4bfb7-110">Un sistema de tipos permite que la sintaxis de una solicitud se presente visualmente de una manera que los desarrolladores comprenden fácilmente y permite que la solicitud se codifique de forma coherente para su transmisión a través de una red.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="4bfb7-111">Para obtener más información acerca de la codificación, vea [reglas de codificación distinguida](distinguished-encoding-rules.md).</span><span class="sxs-lookup"><span data-stu-id="4bfb7-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="4bfb7-112">Para obtener más información sobre los tipos ASN. 1, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="4bfb7-113">Tipos básicos</span><span class="sxs-lookup"><span data-stu-id="4bfb7-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="4bfb7-114">Describe los tipos de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-114">Discusses the following data types:</span></span>

* <span data-ttu-id="4bfb7-115">**CADENA DE BITS**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-115">**BIT STRING**</span></span>
* <span data-ttu-id="4bfb7-116">**BOOLEANO**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-116">**BOOLEAN**</span></span>
* <span data-ttu-id="4bfb7-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-117">**INTEGER**</span></span>
* <span data-ttu-id="4bfb7-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-118">**NULL**</span></span>
* <span data-ttu-id="4bfb7-119">**IDENTIFICADOR DE OBJETO**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="4bfb7-120">**CADENA DE OCTETO**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-120">**OCTET STRING**</span></span>

[<span data-ttu-id="4bfb7-121">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="4bfb7-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="4bfb7-122">Describe los tipos de cadena siguientes:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-122">Discusses the following string types:</span></span>

* <span data-ttu-id="4bfb7-123">**BMPString**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-123">**BMPString**</span></span>
* <span data-ttu-id="4bfb7-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-124">**IA5String**</span></span>
* <span data-ttu-id="4bfb7-125">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-125">**PrintableString**</span></span>
* <span data-ttu-id="4bfb7-126">**TeletexString**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-126">**TeletexString**</span></span>
* <span data-ttu-id="4bfb7-127">**UTF8String**</span><span class="sxs-lookup"><span data-stu-id="4bfb7-127">**UTF8String**</span></span>

[<span data-ttu-id="4bfb7-128">Tipos construidos</span><span class="sxs-lookup"><span data-stu-id="4bfb7-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="4bfb7-129">Describe los tipos de datos ASN. 1 que pueden contener tipos básicos, tipos de cadena u otros tipos construidos.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="4bfb7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bfb7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bfb7-131">Codificación de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="4bfb7-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="4bfb7-132">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4bfb7-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="4bfb7-133">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="4bfb7-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="4bfb7-134">Introducción a la codificación y sintaxis de ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4bfb7-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




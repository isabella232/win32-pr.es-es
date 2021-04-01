---
description: La API de inscripción de certificados usa la notación de sintaxis abstracta uno (ASN. 1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introducción a la codificación y sintaxis de ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909649"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="83f59-103">Introducción a la codificación y sintaxis de ASN. 1</span><span class="sxs-lookup"><span data-stu-id="83f59-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="83f59-104">La API de inscripción de certificados usa la notación de sintaxis abstracta uno (ASN. 1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación.</span><span class="sxs-lookup"><span data-stu-id="83f59-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="83f59-105">ASN. 1 se puede dividir conceptualmente en un conjunto de reglas de sintaxis y un conjunto de reglas de codificación, tal y como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="83f59-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="83f59-106">Ejemplo de sintaxis ASN. 1</span><span class="sxs-lookup"><span data-stu-id="83f59-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="83f59-107">Una solicitud de certificado contiene, entre otras cosas, el nombre de la entidad que realiza la solicitud o para la que se realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f59-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="83f59-108">El nombre es una secuencia de nombres distintivos relativos (RDN) de X. 500.</span><span class="sxs-lookup"><span data-stu-id="83f59-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="83f59-109">Cada RDN de la secuencia consta de un identificador de objeto (OID) y un valor.</span><span class="sxs-lookup"><span data-stu-id="83f59-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="83f59-110">En el ejemplo siguiente se muestra la sintaxis ASN. 1 para un nombre de sujeto.</span><span class="sxs-lookup"><span data-stu-id="83f59-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="83f59-111">Ejemplo de codificación ASN. 1</span><span class="sxs-lookup"><span data-stu-id="83f59-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="83f59-112">La API de inscripción de certificados usa [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der) para codificar el nombre de sujeto anterior.</span><span class="sxs-lookup"><span data-stu-id="83f59-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="83f59-113">DER requiere que cada elemento del nombre se represente mediante un tripledo TLV, donde T contiene el número de etiqueta del tipo ASN. 1, L contiene la longitud y V contiene el valor asociado.</span><span class="sxs-lookup"><span data-stu-id="83f59-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="83f59-114">En el ejemplo siguiente se muestra cómo se codifica el nombre de sujeto TestCN. TestOrg.</span><span class="sxs-lookup"><span data-stu-id="83f59-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="83f59-115">Tenga en cuenta los siguientes puntos:</span><span class="sxs-lookup"><span data-stu-id="83f59-115">Note the following points:</span></span>

-   <span data-ttu-id="83f59-116">Línea 1:</span><span class="sxs-lookup"><span data-stu-id="83f59-116">Line 1:</span></span><dl> <span data-ttu-id="83f59-117">El nombre es una secuencia de nombres distintivos relativos.</span><span class="sxs-lookup"><span data-stu-id="83f59-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="83f59-118">El número de etiqueta del tipo de **secuencia** es 0x30.</span><span class="sxs-lookup"><span data-stu-id="83f59-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="83f59-119">El nombre de sujeto de TestCN. TestOrg requiere 35 (0x23) bytes.</span><span class="sxs-lookup"><span data-stu-id="83f59-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="83f59-120">El nombre común, TestCN, es un único conjunto de estructuras **AttributeTypeValue** .</span><span class="sxs-lookup"><span data-stu-id="83f59-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="83f59-121">El número de etiqueta de un **conjunto** es 0x31.</span><span class="sxs-lookup"><span data-stu-id="83f59-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="83f59-122">
-   Línea 3:</span><span class="sxs-lookup"><span data-stu-id="83f59-122">
-   Line 3:</span></span><dl> <span data-ttu-id="83f59-123">La estructura **AttributeTypeValue** es una secuencia.</span><span class="sxs-lookup"><span data-stu-id="83f59-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="83f59-124">El número de etiqueta del tipo de **secuencia** es 0x30.</span><span class="sxs-lookup"><span data-stu-id="83f59-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="83f59-125">La estructura requiere 13 (0xD) bytes.</span><span class="sxs-lookup"><span data-stu-id="83f59-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="83f59-126">
-   Líneas 4 a 6:</span><span class="sxs-lookup"><span data-stu-id="83f59-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="83f59-127">El identificador de objeto (OID) para el nombre común es 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="83f59-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="83f59-128">El OID es un tipo de **\_ identificador de objeto** de tres bytes.</span><span class="sxs-lookup"><span data-stu-id="83f59-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="83f59-129">El número de etiqueta para el tipo de **\_ ID** . de objeto es 0x06.</span><span class="sxs-lookup"><span data-stu-id="83f59-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="83f59-130">
-   Líneas 7 a 9:</span><span class="sxs-lookup"><span data-stu-id="83f59-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="83f59-131">El nombre común, TestCN, es un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="83f59-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="83f59-132">La cadena es un tipo de **\_ cadena imprimible** de seis bytes.</span><span class="sxs-lookup"><span data-stu-id="83f59-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="83f59-133">El número de etiqueta para el tipo de **\_ cadena imprimible** es 0x13.</span><span class="sxs-lookup"><span data-stu-id="83f59-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="83f59-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83f59-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83f59-135">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="83f59-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="83f59-136">Codificación de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="83f59-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="83f59-137">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="83f59-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="83f59-138">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="83f59-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 

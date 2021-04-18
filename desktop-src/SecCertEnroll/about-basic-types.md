---
description: La API de inscripción de certificados admite los siguientes tipos básicos ASN. 1.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648381"
---
# <a name="basic-types"></a><span data-ttu-id="89647-103">Tipos básicos</span><span class="sxs-lookup"><span data-stu-id="89647-103">Basic Types</span></span>

<span data-ttu-id="89647-104">La API de inscripción de certificados admite los siguientes tipos básicos ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="89647-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="89647-105">CADENA DE BITS</span><span class="sxs-lookup"><span data-stu-id="89647-105">BIT STRING</span></span>

<span data-ttu-id="89647-106">Etiqueta de codificación: 0x03</span><span class="sxs-lookup"><span data-stu-id="89647-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="89647-107">Nombre de Certreq.exe: \_ cadena de bits</span><span class="sxs-lookup"><span data-stu-id="89647-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="89647-108">Un bit o una cadena binaria es una matriz arbitrariamente larga de bits.</span><span class="sxs-lookup"><span data-stu-id="89647-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="89647-109">Los bits específicos se pueden identificar mediante enteros entre paréntesis y nombres asignados, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="89647-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="89647-110">Las firmas y las claves de certificado suelen representarse como cadenas de bits.</span><span class="sxs-lookup"><span data-stu-id="89647-110">Certificate keys and signatures are often represented as bit strings.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a><span data-ttu-id="89647-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="89647-111">BOOLEAN</span></span>

<span data-ttu-id="89647-112">Etiqueta de codificación: 0x01</span><span class="sxs-lookup"><span data-stu-id="89647-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="89647-113">Nombre de Certreq.exe: BOOLEANO</span><span class="sxs-lookup"><span data-stu-id="89647-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="89647-114">Un tipo booleano puede contener uno de dos valores: **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="89647-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="89647-115">En el ejemplo siguiente se muestra la estructura ASN. 1 para una extensión de certificado de restricciones básicas.</span><span class="sxs-lookup"><span data-stu-id="89647-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="89647-116">El campo **CA** especifica si un sujeto de certificado es una entidad de certificación (CA).</span><span class="sxs-lookup"><span data-stu-id="89647-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="89647-117">La importancia predeterminada es **false**.</span><span class="sxs-lookup"><span data-stu-id="89647-117">The default criticality is **FALSE**.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a><span data-ttu-id="89647-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="89647-118">INTEGER</span></span>

<span data-ttu-id="89647-119">Etiqueta de codificación: 0x02</span><span class="sxs-lookup"><span data-stu-id="89647-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="89647-120">Nombre de Certreq.exe: entero</span><span class="sxs-lookup"><span data-stu-id="89647-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="89647-121">Normalmente, un entero puede ser cualquier valor entero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="89647-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="89647-122">En el ejemplo siguiente se muestra la estructura ASN. 1 para una clave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="89647-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="89647-123">Tenga en cuenta que el campo **publicExponent** está restringido a un entero positivo inferior a 4.294.967.296.</span><span class="sxs-lookup"><span data-stu-id="89647-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a><span data-ttu-id="89647-124">NULL</span><span class="sxs-lookup"><span data-stu-id="89647-124">NULL</span></span>

<span data-ttu-id="89647-125">Etiqueta de codificación: 0x05</span><span class="sxs-lookup"><span data-stu-id="89647-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="89647-126">Nombre de Certreq.exe: **null**</span><span class="sxs-lookup"><span data-stu-id="89647-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="89647-127">Un tipo **nulo** contiene un solo byte 0x00.</span><span class="sxs-lookup"><span data-stu-id="89647-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="89647-128">Se puede utilizar en cualquier lugar en el que la solicitud de certificado debe indicar un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="89647-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="89647-129">Por ejemplo, un **AlgorithmIdentifier** es una secuencia que contiene un identificador de objeto (OID) y parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="89647-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

<span data-ttu-id="89647-130">Si no hay ningún parámetro cuando la estructura está codificada, se utiliza **null** para indicar un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="89647-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="89647-131">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="89647-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="89647-132">Etiqueta de codificación: 0x06</span><span class="sxs-lookup"><span data-stu-id="89647-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="89647-133">Nombre del Certreq.exe: \_ ID. de objeto</span><span class="sxs-lookup"><span data-stu-id="89647-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="89647-134">La API de inscripción de certificados utiliza identificadores de objeto (OID) como un tipo de puntero universal a identificadores de algoritmo, atributos y otros elementos de PKI.</span><span class="sxs-lookup"><span data-stu-id="89647-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="89647-135">Normalmente, los OID se presentan en una cadena decimal con puntos como "2.16.840.1.101.3.4.1.42".</span><span class="sxs-lookup"><span data-stu-id="89647-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="89647-136">Los elementos individuales de la cadena, separados por puntos, representan los arcos y salen de un árbol de autoridad de registro que identifica de forma única el objeto y la organización que lo registró.</span><span class="sxs-lookup"><span data-stu-id="89647-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="89647-137">Por ejemplo, el OID anterior se puede expandir a Joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) con. 42 anexado para identificar de forma única el algoritmo del modo de cifrado de bloques de cifrado (CBC) AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="89647-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a><span data-ttu-id="89647-138">CADENA DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="89647-138">OCTET STRING</span></span>

<span data-ttu-id="89647-139">Etiqueta de codificación: 0x04</span><span class="sxs-lookup"><span data-stu-id="89647-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="89647-140">Nombre de Certreq.exe: \_ cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="89647-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="89647-141">Una cadena de octetos es una matriz de bytes arbitrariamente grande.</span><span class="sxs-lookup"><span data-stu-id="89647-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="89647-142">A diferencia del tipo de **cadena de bits** , sin embargo, los bits y bytes específicos de la cadena no pueden tener nombres asignados.</span><span class="sxs-lookup"><span data-stu-id="89647-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="89647-143">La palabra octet está pensada como una manera independiente de la plataforma de hacer referencia a una palabra de memoria.</span><span class="sxs-lookup"><span data-stu-id="89647-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="89647-144">En el contexto de la API de inscripción de certificados, octeto y byte son intercambiables.</span><span class="sxs-lookup"><span data-stu-id="89647-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a><span data-ttu-id="89647-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89647-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89647-146">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="89647-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="89647-147">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="89647-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="89647-148">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="89647-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




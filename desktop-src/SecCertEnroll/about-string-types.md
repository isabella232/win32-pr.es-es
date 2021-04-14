---
description: Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276806"
---
# <a name="string-types"></a><span data-ttu-id="b6bc4-103">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="b6bc4-103">String Types</span></span>

<span data-ttu-id="b6bc4-104">Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X. 500.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="b6bc4-105">Por ejemplo, el nombre de sujeto de una solicitud de certificado se crea mediante la combinación de una secuencia de nombres distintivos relativos, tal y como se muestra en el siguiente ejemplo de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="b6bc4-106">La API de inscripción de certificados admite los siguientes tipos de cadena ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="b6bc4-107">BMPString</span><span class="sxs-lookup"><span data-stu-id="b6bc4-107">BMPString</span></span>

<span data-ttu-id="b6bc4-108">Etiqueta de codificación: 0x1E</span><span class="sxs-lookup"><span data-stu-id="b6bc4-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="b6bc4-109">Nombre de Certreq.exe: cadena Unicode \_</span><span class="sxs-lookup"><span data-stu-id="b6bc4-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="b6bc4-110">El plano básico multilingüe (BMP) es una codificación de caracteres que engloba el primer plano del juego de caracteres universal (UCS).</span><span class="sxs-lookup"><span data-stu-id="b6bc4-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="b6bc4-111">Hay diecisiete planos numerados de 0 a 16.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="b6bc4-112">BMP ocupa el plano 0 e incluye 65.536 puntos de código entre 0x0000 y 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="b6bc4-113">Esta es la sección del mapa de caracteres Unicode, donde la mayoría de los caracteres asignados se han realizado hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="b6bc4-114">Incluye Latin, Oriente Medio, asiático, África y otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="b6bc4-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="b6bc4-115">IA5String</span></span>

<span data-ttu-id="b6bc4-116">Etiqueta de codificación: 0x16</span><span class="sxs-lookup"><span data-stu-id="b6bc4-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="b6bc4-117">Nombre de Certreq.exe: IA5 \_ cadena</span><span class="sxs-lookup"><span data-stu-id="b6bc4-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="b6bc4-118">El alfabeto internacional número 5 (IA5) suele ser equivalente al alfabeto ASCII, pero las distintas versiones pueden incluir Acentos u otros caracteres específicos de un idioma regional.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="b6bc4-119">En el ejemplo siguiente se muestra el tipo **IA5String** que se usa en la definición de ASN. 1 de la extensión de certificado **AlternativeNames** .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a><span data-ttu-id="b6bc4-120">PrintableString</span><span class="sxs-lookup"><span data-stu-id="b6bc4-120">PrintableString</span></span>

<span data-ttu-id="b6bc4-121">Etiqueta de codificación: 0x13</span><span class="sxs-lookup"><span data-stu-id="b6bc4-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="b6bc4-122">Nombre de Certreq.exe: cadena IMPRIMIble \_</span><span class="sxs-lookup"><span data-stu-id="b6bc4-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="b6bc4-123">El tipo de datos **PrintableString** se diseñó originalmente para representar los juegos de caracteres limitados disponibles para los terminales de entrada de mainframe, pero se suele usar.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="b6bc4-124">Contiene los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="b6bc4-124">It contains the following characters:</span></span>

-   <span data-ttu-id="b6bc4-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="b6bc4-125">A-Z</span></span>
-   <span data-ttu-id="b6bc4-126">a-z</span><span class="sxs-lookup"><span data-stu-id="b6bc4-126">a-z</span></span>
-   <span data-ttu-id="b6bc4-127">0-9</span><span class="sxs-lookup"><span data-stu-id="b6bc4-127">0-9</span></span>
-   <span data-ttu-id="b6bc4-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-128">' ( ) + , - .</span></span> <span data-ttu-id="b6bc4-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="b6bc4-129">/ : = ?</span></span> <span data-ttu-id="b6bc4-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="b6bc4-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="b6bc4-131">TeletexString</span><span class="sxs-lookup"><span data-stu-id="b6bc4-131">TeletexString</span></span>

<span data-ttu-id="b6bc4-132">Etiqueta de codificación: 0x14</span><span class="sxs-lookup"><span data-stu-id="b6bc4-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="b6bc4-133">Los tipos de datos **TeletexString** y **T61String** relacionados se codifican en 8 bits (o 16 bits para caracteres compuestos).</span><span class="sxs-lookup"><span data-stu-id="b6bc4-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="b6bc4-134">Ambos tienen un número de etiqueta de 0x14.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="b6bc4-135">No se usan exhaustivamente.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="b6bc4-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="b6bc4-136">UTF8String</span></span>

<span data-ttu-id="b6bc4-137">Etiqueta de codificación: 0x0C</span><span class="sxs-lookup"><span data-stu-id="b6bc4-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="b6bc4-138">Nombre de la Certreq.exe: UTF8 \_ cadena</span><span class="sxs-lookup"><span data-stu-id="b6bc4-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="b6bc4-139">El formato de transformación UCS/Unicode (UTF-8) de 8 bits es una codificación de caracteres de longitud variable que puede representar cualquier carácter universal como carácter Unicode, al tiempo que permite que los puntos de código iniciales sigan siendo coherentes con ASCII.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="b6bc4-140">UTF-8 usa de uno a cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="b6bc4-141">El número de etiqueta es 0x0C.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6bc4-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6bc4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6bc4-143">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="b6bc4-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="b6bc4-144">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="b6bc4-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="b6bc4-145">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="b6bc4-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




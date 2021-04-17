---
description: Un tipo de notación de sintaxis abstracta (ASN. 1) construido se compone de tipos básicos, tipos de cadena u otros tipos construidos. Por ejemplo, una extensión de certificado X. 509 se compone de tres tipos básicos ASN. 1, tal y como se muestra en el ejemplo siguiente.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipos construidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666424"
---
# <a name="constructed-types"></a><span data-ttu-id="56970-104">Tipos construidos</span><span class="sxs-lookup"><span data-stu-id="56970-104">Constructed Types</span></span>

<span data-ttu-id="56970-105">Un tipo de [*notación de sintaxis abstracta*](/windows/desktop/SecGloss/a-gly) (ASN. 1) construido se compone de tipos básicos, tipos de cadena u otros tipos construidos.</span><span class="sxs-lookup"><span data-stu-id="56970-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="56970-106">Por ejemplo, una extensión de certificado X. 509 se compone de tres tipos básicos ASN. 1, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56970-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="56970-107">Una extensión consta de un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) (OID), un valor booleano que identifica si la extensión es crítica y una matriz de bytes que contiene el valor.</span><span class="sxs-lookup"><span data-stu-id="56970-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="56970-108">La API de inscripción de certificados admite los siguientes tipos de ASN. 1 construidos.</span><span class="sxs-lookup"><span data-stu-id="56970-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="56970-109">SECUENCIA y secuencia de</span><span class="sxs-lookup"><span data-stu-id="56970-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="56970-110">Etiqueta de codificación: 0x30</span><span class="sxs-lookup"><span data-stu-id="56970-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="56970-111">Contiene una serie ordenada de campos de uno o más tipos.</span><span class="sxs-lookup"><span data-stu-id="56970-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="56970-112">Los campos se pueden marcar como **opcionales** o como **valores predeterminados**.</span><span class="sxs-lookup"><span data-stu-id="56970-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="56970-113">Además, para evitar ambigüedades al descodificar, los campos opcionales sucesivos deben ser diferentes entre sí mediante el uso de un identificador único (un entero entre corchetes como \[ 1 \] ) y de un campo obligatorio siguiente, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56970-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="56970-114">La diferencia entre **Sequence** y **sequence of** es que los elementos de una **secuencia de** construcción deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="56970-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="56970-115">Consulte el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="56970-115">See the following example.</span></span> <span data-ttu-id="56970-116">Ambas construcciones tienen el mismo valor de etiqueta (0x30) cuando se codifican.</span><span class="sxs-lookup"><span data-stu-id="56970-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="56970-117">Otra manera de examinar la diferencia entre **Sequence** y **sequence of** es compararlas con sus homólogos en el lenguaje de programación C.</span><span class="sxs-lookup"><span data-stu-id="56970-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="56970-118">Es decir, la **secuencia** es aproximadamente equivalente a una estructura y la **secuencia de** es aproximadamente equivalente a una matriz.</span><span class="sxs-lookup"><span data-stu-id="56970-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="56970-119">ESTABLECER y establecer</span><span class="sxs-lookup"><span data-stu-id="56970-119">SET and SET OF</span></span>

<span data-ttu-id="56970-120">Etiqueta de codificación: 0x31</span><span class="sxs-lookup"><span data-stu-id="56970-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="56970-121">Contiene una serie desordenada de campos de uno o más tipos.</span><span class="sxs-lookup"><span data-stu-id="56970-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="56970-122">Esto difiere de una **secuencia** que contiene una lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="56970-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="56970-123">La especificación de una lista sin ordenar permite a una aplicación proporcionar los campos de la estructura al codificador en el orden más adecuado.</span><span class="sxs-lookup"><span data-stu-id="56970-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="56970-124">Como con **Sequence**, los campos de una construcción **set** se pueden marcar con **Optional** o **default**, y los identificadores únicos deben usarse para eliminar la ambigüedad del proceso de descodificación.</span><span class="sxs-lookup"><span data-stu-id="56970-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="56970-125">La diferencia entre **set** y **set de** es que los elementos de un **conjunto de** construcciones deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="56970-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="56970-126">ALTERNATIVA</span><span class="sxs-lookup"><span data-stu-id="56970-126">CHOICE</span></span>

<span data-ttu-id="56970-127">Etiqueta de codificación: no aplicable</span><span class="sxs-lookup"><span data-stu-id="56970-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="56970-128">Define una opción entre alternativas.</span><span class="sxs-lookup"><span data-stu-id="56970-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="56970-129">Cada alternativa se debe identificar de forma única mediante un entero entre corchetes para evitar la ambigüedad al descodificar.</span><span class="sxs-lookup"><span data-stu-id="56970-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="56970-130">Cuando se codifica, la construcción **Choice** tendrá el valor de la etiqueta de codificación de la alternativa elegida.</span><span class="sxs-lookup"><span data-stu-id="56970-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a><span data-ttu-id="56970-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56970-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56970-132">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="56970-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="56970-133">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="56970-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="56970-134">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="56970-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 

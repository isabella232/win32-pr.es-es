---
description: Un certificado X. 509 versión 1 contiene los siguientes campos. Los campos de la versión 2 se describen en los campos de la versión 2. Los campos de la versión 3 se describen en extensiones de la versión 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909654"
---
# <a name="basic-fields"></a><span data-ttu-id="7773f-105">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="7773f-105">Basic Fields</span></span>

<span data-ttu-id="7773f-106">Un certificado X. 509 versión 1 contiene los siguientes campos.</span><span class="sxs-lookup"><span data-stu-id="7773f-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="7773f-107">Los campos de la versión 2 se describen en [los campos de la versión 2](about-version-2-fields.md).</span><span class="sxs-lookup"><span data-stu-id="7773f-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="7773f-108">Los campos de la versión 3 se describen en extensiones de la [versión 3](about-version-3-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="7773f-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="7773f-109">Versión</span><span class="sxs-lookup"><span data-stu-id="7773f-109">Version</span></span>

<span data-ttu-id="7773f-110">Especifica el número de versión del certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="7773f-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="7773f-111">Actualmente, los valores posibles de este campo son 0, 1 o 2, pero se pueden expandir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="7773f-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="7773f-112">Número de serie</span><span class="sxs-lookup"><span data-stu-id="7773f-112">Serial Number</span></span>

<span data-ttu-id="7773f-113">Contiene un entero positivo único asignado por la entidad de certificación (CA) al certificado.</span><span class="sxs-lookup"><span data-stu-id="7773f-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="7773f-114">Algoritmo de firma</span><span class="sxs-lookup"><span data-stu-id="7773f-114">Signature Algorithm</span></span>

<span data-ttu-id="7773f-115">Contiene un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) (OID) que especifica el algoritmo utilizado por la entidad de certificación para firmar el certificado.</span><span class="sxs-lookup"><span data-stu-id="7773f-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="7773f-116">Por ejemplo, 1.2.840.113549.1.1.5 especifica un algoritmo hash SHA-1 combinado con el algoritmo de cifrado RSA de RSA Laboratories.</span><span class="sxs-lookup"><span data-stu-id="7773f-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a><span data-ttu-id="7773f-117">Emisor</span><span class="sxs-lookup"><span data-stu-id="7773f-117">Issuer</span></span>

<span data-ttu-id="7773f-118">Contiene el nombre distintivo (DN) [*X. 500*](/windows/desktop/SecGloss/x-gly) de la entidad de certificación que creó y firmó el certificado.</span><span class="sxs-lookup"><span data-stu-id="7773f-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a><span data-ttu-id="7773f-119">Validez</span><span class="sxs-lookup"><span data-stu-id="7773f-119">Validity</span></span>

<span data-ttu-id="7773f-120">Especifica el intervalo de tiempo durante el cual el certificado es válido.</span><span class="sxs-lookup"><span data-stu-id="7773f-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="7773f-121">Las fechas hasta el final de 2049 usan el formato de hora universal coordinada (hora del meridiano de Greenwich) (*yymmddhhmmssz*).</span><span class="sxs-lookup"><span data-stu-id="7773f-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="7773f-122">Las fechas a partir del 1 de enero de 2050 usan el formato de hora generalizada (*yyyymmddhhmmssz*).</span><span class="sxs-lookup"><span data-stu-id="7773f-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a><span data-ttu-id="7773f-123">Asunto</span><span class="sxs-lookup"><span data-stu-id="7773f-123">Subject</span></span>

<span data-ttu-id="7773f-124">Contiene un nombre distintivo X.500 de la entidad asociada con la clave pública contenida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="7773f-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a><span data-ttu-id="7773f-125">Clave pública</span><span class="sxs-lookup"><span data-stu-id="7773f-125">Public Key</span></span>

<span data-ttu-id="7773f-126">Contiene la clave pública y la información de algoritmo asociada.</span><span class="sxs-lookup"><span data-stu-id="7773f-126">Contains the public key and associated algorithm information.</span></span>

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a><span data-ttu-id="7773f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7773f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7773f-128">Campos de la versión 2</span><span class="sxs-lookup"><span data-stu-id="7773f-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="7773f-129">Extensiones de la versión 3</span><span class="sxs-lookup"><span data-stu-id="7773f-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="7773f-130">Certificados de clave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="7773f-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 

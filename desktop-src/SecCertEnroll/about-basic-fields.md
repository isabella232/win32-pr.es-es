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
# <a name="basic-fields"></a>Campos básicos

Un certificado X. 509 versión 1 contiene los siguientes campos. Los campos de la versión 2 se describen en [los campos de la versión 2](about-version-2-fields.md). Los campos de la versión 3 se describen en extensiones de la [versión 3](about-version-3-extensions.md).

## <a name="version"></a>Versión

Especifica el número de versión del certificado codificado. Actualmente, los valores posibles de este campo son 0, 1 o 2, pero se pueden expandir en el futuro.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Número de serie

Contiene un entero positivo único asignado por la entidad de certificación (CA) al certificado.

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Algoritmo de firma

Contiene un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) (OID) que especifica el algoritmo utilizado por la entidad de certificación para firmar el certificado. Por ejemplo, 1.2.840.113549.1.1.5 especifica un algoritmo hash SHA-1 combinado con el algoritmo de cifrado RSA de RSA Laboratories.

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

## <a name="issuer"></a>Emisor

Contiene el nombre distintivo (DN) [*X. 500*](/windows/desktop/SecGloss/x-gly) de la entidad de certificación que creó y firmó el certificado.

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

## <a name="validity"></a>Validez

Especifica el intervalo de tiempo durante el cual el certificado es válido. Las fechas hasta el final de 2049 usan el formato de hora universal coordinada (hora del meridiano de Greenwich) (*yymmddhhmmssz*). Las fechas a partir del 1 de enero de 2050 usan el formato de hora generalizada (*yyyymmddhhmmssz*).

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

## <a name="subject"></a>Asunto

Contiene un nombre distintivo X.500 de la entidad asociada con la clave pública contenida en el certificado.

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

## <a name="public-key"></a>Clave pública

Contiene la clave pública y la información de algoritmo asociada.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Campos de la versión 2](about-version-2-fields.md)
</dt> <dt>

[Extensiones de la versión 3](about-version-3-extensions.md)
</dt> <dt>

[Certificados de clave pública X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 

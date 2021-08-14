---
description: La API de inscripción de certificados admite los siguientes tipos básicos de ASN.1.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905050"
---
# <a name="basic-types"></a>Tipos básicos

La API de inscripción de certificados admite los siguientes tipos básicos de ASN.1.

## <a name="bit-string"></a>CADENA DE BITS

Etiqueta de codificación: 0x03

Certreq.exe nombre: BIT \_ STRING

Una cadena binaria o de bits es una matriz arbitrariamente larga de bits. Los bits específicos se pueden identificar mediante enteros entre paréntesis y nombres asignados, como en el ejemplo siguiente.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Las claves de certificado y las firmas se suelen representar como cadenas de bits.

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

## <a name="boolean"></a>BOOLEAN

Etiqueta de codificación: 0x01

Certreq.exe nombre: BOOLEAN

Un tipo booleano puede contener uno de dos valores, **TRUE** o **FALSE.** En el ejemplo siguiente se muestra la estructura ASN.1 para una extensión de certificado Restricciones básicas. El **campo cA** especifica si un sujeto de certificado es una entidad de certificación (CA). La importancia crítica predeterminada es **FALSE.**

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

## <a name="integer"></a>INTEGER

Etiqueta de codificación: 0x02

Certreq.exe nombre: INTEGER

Normalmente, un entero puede ser cualquier valor entero positivo o negativo. En el ejemplo siguiente se muestra la estructura ASN.1 para una clave pública RSA. Tenga en cuenta **que el campo publicExponent** está restringido a un entero positivo inferior a 4 294 967 296.

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

## <a name="null"></a>NULL

Etiqueta de codificación: 0x05

Certreq.exe nombre: **NULL**

Un **tipo NULL** contiene un solo byte 0x00. Se puede usar en cualquier lugar en el que la solicitud de certificado deba indicar un valor vacío. Por ejemplo, **algorithmidentifier es** una secuencia que contiene un identificador de objeto (OID) y parámetros opcionales.

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

Si no hay ningún parámetro cuando se codifica la estructura, se usa **NULL** para indicar un valor vacío.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICADOR DE OBJETO

Etiqueta de codificación: 0x06

Certreq.exe nombre: IDENTIFICADOR DE \_ OBJETO

La API de inscripción de certificados usa identificadores de objeto ( IDENTIFICADORES) como un tipo de puntero universal a identificadores de algoritmo, atributos y otros elementos PKI. Normalmente, los EDI se presentan en una cadena decimal con puntos, como "2.16.840.1.101.3.4.1.42". Los elementos individuales de la cadena, separados por puntos, representan los arcos y hojas en un árbol de autoridad de registro que identifica de forma única el objeto y la organización que lo registró. Por ejemplo, el OID anterior se puede expandir a joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.

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

## <a name="octet-string"></a>OCTET STRING

Etiqueta de codificación: 0x04

Certreq.exe nombre: OCTET \_ STRING

Una cadena de octeto es una matriz de bytes arbitrariamente grande. Sin embargo, a diferencia del tipo **BIT STRING,** no se pueden asignar nombres a bits y bytes específicos de la cadena. La palabra octeto está pensada para ser una manera independiente de la plataforma de hacer referencia a una palabra de memoria. En el contexto de la API de inscripción de certificados, el octeto y el byte son intercambiables.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




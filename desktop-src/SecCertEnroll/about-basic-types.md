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
# <a name="basic-types"></a>Tipos básicos

La API de inscripción de certificados admite los siguientes tipos básicos ASN. 1.

## <a name="bit-string"></a>CADENA DE BITS

Etiqueta de codificación: 0x03

Nombre de Certreq.exe: \_ cadena de bits

Un bit o una cadena binaria es una matriz arbitrariamente larga de bits. Los bits específicos se pueden identificar mediante enteros entre paréntesis y nombres asignados, como en el ejemplo siguiente.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Las firmas y las claves de certificado suelen representarse como cadenas de bits.

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

Nombre de Certreq.exe: BOOLEANO

Un tipo booleano puede contener uno de dos valores: **true** o **false**. En el ejemplo siguiente se muestra la estructura ASN. 1 para una extensión de certificado de restricciones básicas. El campo **CA** especifica si un sujeto de certificado es una entidad de certificación (CA). La importancia predeterminada es **false**.

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

Nombre de Certreq.exe: entero

Normalmente, un entero puede ser cualquier valor entero positivo o negativo. En el ejemplo siguiente se muestra la estructura ASN. 1 para una clave pública RSA. Tenga en cuenta que el campo **publicExponent** está restringido a un entero positivo inferior a 4.294.967.296.

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

Nombre de Certreq.exe: **null**

Un tipo **nulo** contiene un solo byte 0x00. Se puede utilizar en cualquier lugar en el que la solicitud de certificado debe indicar un valor vacío. Por ejemplo, un **AlgorithmIdentifier** es una secuencia que contiene un identificador de objeto (OID) y parámetros opcionales.

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

Si no hay ningún parámetro cuando la estructura está codificada, se utiliza **null** para indicar un valor vacío.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICADOR DE OBJETO

Etiqueta de codificación: 0x06

Nombre del Certreq.exe: \_ ID. de objeto

La API de inscripción de certificados utiliza identificadores de objeto (OID) como un tipo de puntero universal a identificadores de algoritmo, atributos y otros elementos de PKI. Normalmente, los OID se presentan en una cadena decimal con puntos como "2.16.840.1.101.3.4.1.42". Los elementos individuales de la cadena, separados por puntos, representan los arcos y salen de un árbol de autoridad de registro que identifica de forma única el objeto y la organización que lo registró. Por ejemplo, el OID anterior se puede expandir a Joint-ISO-ITU-t (2) Country (16) US (840) Organization (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) con. 42 anexado para identificar de forma única el algoritmo del modo de cifrado de bloques de cifrado (CBC) AES de 256 bits.

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

## <a name="octet-string"></a>CADENA DE OCTETO

Etiqueta de codificación: 0x04

Nombre de Certreq.exe: \_ cadena de octeto

Una cadena de octetos es una matriz de bytes arbitrariamente grande. A diferencia del tipo de **cadena de bits** , sin embargo, los bits y bytes específicos de la cadena no pueden tener nombres asignados. La palabra octet está pensada como una manera independiente de la plataforma de hacer referencia a una palabra de memoria. En el contexto de la API de inscripción de certificados, octeto y byte son intercambiables.

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

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




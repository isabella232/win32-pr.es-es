---
description: El concepto de un tipo de datos es fundamental para el estándar abstract Syntax Notation One (ASN.1).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema de tipo ASN.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0b5b9780057229d301bbabcdf2484c66bf06b4313587b0e70a68070885a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905080"
---
# <a name="asn1-type-system"></a>Sistema de tipo ASN.1

El concepto de un tipo de datos es fundamental para el estándar abstract Syntax Notation One (ASN.1). Cada campo de una estructura de solicitud de certificado está asociado a un tipo. Considere, por ejemplo, la sintaxis de certificado PKCS \# 10 ASN.1 que se muestra en el ejemplo siguiente.

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

La estructura de solicitudes de alto **nivel, CertificationRequestInfo,** es un tipo que se forma a partir de una secuencia de otros tipos. Cuando un tipo es o solo contiene tipos básicos, tipos de cadena o **ANY**, no se puede desglosar aún más. Por ejemplo,  el campo de versión es un tipo **CertificationRequestInfoVersion** que, a su vez, es un tipo **INTEGER,** un tipo ASN.1 básico que no se compone de otros tipos.

Un sistema de tipos permite que la sintaxis de una solicitud se presente visualmente de una manera que los desarrolladores entiendan fácilmente, y permite codificar la solicitud de forma coherente para su transmisión a través de una red. Para obtener más información sobre la codificación, [vea reglas de codificación distinguida](distinguished-encoding-rules.md). Para obtener más información sobre los tipos de ASN.1, vea los temas siguientes.

[Tipos básicos](about-basic-types.md)

Describe los siguientes tipos de datos:

* **CADENA DE BITS**
* **Booleana**
* **INTEGER**
* **NULL**
* **IDENTIFICADOR DE OBJETO**
* **OCTET STRING**

[Tipos de cadena](about-string-types.md)

Describe los siguientes tipos de cadena:

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Tipos construidos](about-constructed-types.md)

Describe los tipos de datos ASN.1 que pueden contener tipos básicos, tipos de cadena u otros tipos construidos.




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de solicitud de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Introducción a la sintaxis y codificación de ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




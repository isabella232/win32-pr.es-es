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
# <a name="asn1-type-system"></a>Sistema de tipos ASN. 1

El concepto de un tipo de datos es fundamental para el estándar de notación de sintaxis abstracta uno (ASN. 1). Cada campo de una estructura de solicitud de certificado está asociado a un tipo. Considere, por ejemplo, la \# Sintaxis de certificado PKCS 10 ASN. 1 que se muestra en el ejemplo siguiente.

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

La estructura de solicitud de alto nivel, **CertificationRequestInfo**, es un tipo que se compone de una secuencia de otros tipos. Cuando un tipo es o contiene solo tipos básicos, tipos de cadena o **cualquiera**, no se puede desglosar más. Por ejemplo, el campo **version** es un tipo **CertificationRequestInfoVersion** que, a su vez, es un tipo **entero** , un tipo ASN. 1 básico que no se compone de otros tipos.

Un sistema de tipos permite que la sintaxis de una solicitud se presente visualmente de una manera que los desarrolladores comprenden fácilmente y permite que la solicitud se codifique de forma coherente para su transmisión a través de una red. Para obtener más información acerca de la codificación, vea [reglas de codificación distinguida](distinguished-encoding-rules.md). Para obtener más información sobre los tipos ASN. 1, vea los temas siguientes.

[Tipos básicos](about-basic-types.md)

Describe los tipos de datos siguientes:

* **CADENA DE BITS**
* **BOOLEANO**
* **INTEGER**
* **NULL**
* **IDENTIFICADOR DE OBJETO**
* **CADENA DE OCTETO**

[Tipos de cadena](about-string-types.md)

Describe los tipos de cadena siguientes:

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Tipos construidos](about-constructed-types.md)

Describe los tipos de datos ASN. 1 que pueden contener tipos básicos, tipos de cadena u otros tipos construidos.




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de solicitud de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Introducción a la codificación y sintaxis de ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 




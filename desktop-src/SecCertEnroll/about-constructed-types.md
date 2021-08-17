---
description: Un tipo de notación de sintaxis abstracta uno (ASN.1) construido se consta de tipos básicos, tipos de cadena u otros tipos construidos. Por ejemplo, una extensión de certificado X.509 se compone de tres tipos básicos de ASN.1, como se muestra en el ejemplo siguiente.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipos construidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ed62c4a59bfc0944ad5e31673ab0ea9031c0175014c8fc1c6b6f2cc071b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904494"
---
# <a name="constructed-types"></a>Tipos construidos

Un tipo [*de notación*](/windows/desktop/SecGloss/a-gly) de sintaxis abstracta uno (ASN.1) construido se consta de tipos básicos, tipos de cadena u otros tipos construidos. Por ejemplo, una extensión de certificado X.509 se compone de tres tipos básicos de ASN.1, como se muestra en el ejemplo siguiente.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Una extensión consta de un [*identificador*](/windows/desktop/SecGloss/o-gly) de objeto (OID), un valor booleano que identifica si la extensión es crítica y una matriz de bytes que contiene el valor. La API de inscripción de certificados admite los siguientes tipos ASN.1 construidos.

## <a name="sequence-and-sequence-of"></a>SEQUENCE y SEQUENCE OF

Etiqueta de codificación: 0x30

Contiene una serie ordenada de campos de uno o varios tipos. Los campos se pueden marcar **como OPTIONAL** o **DEFAULT.** Además, para evitar ambigüedades al decodificar, los campos opcionales sucesivos deben diferir entre sí mediante el uso de un identificador único (un entero entre corchetes como 1) y de un campo obligatorio siguiente, como se muestra en el ejemplo \[ \] siguiente.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

La diferencia entre **SEQUENCE** y **SEQUENCE OF** es que los elementos de una construcción **SEQUENCE OF** deben ser del mismo tipo. Consulte el ejemplo siguiente. Ambas construcciones tienen el mismo valor de etiqueta (0x30) cuando se codifican.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Otra manera de ver la diferencia entre **SEQUENCE** y **SEQUENCE OF** es compararlos con sus homólogos en el lenguaje de programación C. Es decir, **SEQUENCE** es aproximadamente equivalente a una estructura y **SEQUENCE OF** es aproximadamente equivalente a una matriz.

## <a name="set-and-set-of"></a>SET y SET OF

Etiqueta de codificación: 0x31

Contiene una serie desordenada de campos de uno o varios tipos. Esto difiere de una **secuencia que** contiene una lista ordenada. La especificación de una lista desordenada permite a una aplicación proporcionar los campos de estructura al codificador en el orden más adecuado. Al igual que **con SEQUENCE**, los campos de una **construcción SET** se pueden marcar con **OPTIONAL** o **DEFAULT,** y los identificadores únicos deben usarse para eliminar la ambigüedad del proceso de descodificado. La diferencia entre **SET** y **SET OF** es que los elementos de una construcción **SET OF** deben ser del mismo tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>Elección

Etiqueta de codificación: no aplicable

Define una opción entre alternativas. Cada alternativa debe identificarse de forma única mediante un entero entre corchetes para evitar ambigüedades alcoding. Cuando se codifica, la **construcción CHOICE** tendrá el valor de etiqueta de codificación de la alternativa elegida.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 

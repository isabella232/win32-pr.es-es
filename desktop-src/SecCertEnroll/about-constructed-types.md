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
# <a name="constructed-types"></a>Tipos construidos

Un tipo de [*notación de sintaxis abstracta*](/windows/desktop/SecGloss/a-gly) (ASN. 1) construido se compone de tipos básicos, tipos de cadena u otros tipos construidos. Por ejemplo, una extensión de certificado X. 509 se compone de tres tipos básicos ASN. 1, tal y como se muestra en el ejemplo siguiente.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Una extensión consta de un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) (OID), un valor booleano que identifica si la extensión es crítica y una matriz de bytes que contiene el valor. La API de inscripción de certificados admite los siguientes tipos de ASN. 1 construidos.

## <a name="sequence-and-sequence-of"></a>SECUENCIA y secuencia de

Etiqueta de codificación: 0x30

Contiene una serie ordenada de campos de uno o más tipos. Los campos se pueden marcar como **opcionales** o como **valores predeterminados**. Además, para evitar ambigüedades al descodificar, los campos opcionales sucesivos deben ser diferentes entre sí mediante el uso de un identificador único (un entero entre corchetes como \[ 1 \] ) y de un campo obligatorio siguiente, tal como se muestra en el ejemplo siguiente.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

La diferencia entre **Sequence** y **sequence of** es que los elementos de una **secuencia de** construcción deben ser del mismo tipo. Consulte el ejemplo siguiente. Ambas construcciones tienen el mismo valor de etiqueta (0x30) cuando se codifican.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Otra manera de examinar la diferencia entre **Sequence** y **sequence of** es compararlas con sus homólogos en el lenguaje de programación C. Es decir, la **secuencia** es aproximadamente equivalente a una estructura y la **secuencia de** es aproximadamente equivalente a una matriz.

## <a name="set-and-set-of"></a>ESTABLECER y establecer

Etiqueta de codificación: 0x31

Contiene una serie desordenada de campos de uno o más tipos. Esto difiere de una **secuencia** que contiene una lista ordenada. La especificación de una lista sin ordenar permite a una aplicación proporcionar los campos de la estructura al codificador en el orden más adecuado. Como con **Sequence**, los campos de una construcción **set** se pueden marcar con **Optional** o **default**, y los identificadores únicos deben usarse para eliminar la ambigüedad del proceso de descodificación. La diferencia entre **set** y **set de** es que los elementos de un **conjunto de** construcciones deben ser del mismo tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>ALTERNATIVA

Etiqueta de codificación: no aplicable

Define una opción entre alternativas. Cada alternativa se debe identificar de forma única mediante un entero entre corchetes para evitar la ambigüedad al descodificar. Cuando se codifica, la construcción **Choice** tendrá el valor de la etiqueta de codificación de la alternativa elegida.

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

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 

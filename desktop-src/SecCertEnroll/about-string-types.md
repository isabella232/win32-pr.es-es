---
description: Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X.500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9e190e10bc86bd68a344f5aa279b4812bc04437418578320c36e0e1791dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903694"
---
# <a name="string-types"></a>Tipos de cadena

Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X.500. Por ejemplo, el nombre del firmante de una solicitud de certificado se crea combinando una secuencia de nombres distintivos relativos, como se muestra en el ejemplo de sintaxis siguiente.

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

La API de inscripción de certificados admite los siguientes tipos de cadena asn.1.

## <a name="bmpstring"></a>BMPString

Etiqueta de codificación: 0x1E

Certreq.exe nombre: CADENA \_ UNICODE

El plano multilingüe básico (BMP) es una codificación de caracteres que abarca el primer plano del juego de caracteres universal (UCS). Hay planos grandes numerados de 0 a 16. BMP ocupa el plano 0 e incluye 65 536 puntos de código de 0x0000 a 0xFFFF. Esta es la sección del mapa de caracteres Unicode donde se han realizado la mayoría de las asignaciones de caracteres hasta ahora. Incluye latín, Oriente Medio, Asia, África y otros idiomas.

## <a name="ia5string"></a>IA5String

Etiqueta de codificación: 0x16

Certreq.exe nombre: IA5 \_ STRING

El alfabeto internacional número 5 (IA5) suele ser equivalente al alfabeto ASCII, pero las distintas versiones pueden incluir acentos u otros caracteres específicos de un idioma regional. En el ejemplo siguiente se muestra **el tipo IA5String** usado en la definición de ASN.1 de la **extensión de certificado AlternativeNames.**

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

## <a name="printablestring"></a>PrintableString

Etiqueta de codificación: 0x13

Certreq.exe nombre: \_ CADENA IMPRIMIBLE

El **tipo de datos PrintableString** estaba pensado originalmente para representar los conjuntos de caracteres limitados disponibles para los terminales de entrada del sistema central, pero se sigue utilizando normalmente. Contiene los caracteres siguientes:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Etiqueta de codificación: 0x14

Los **tipos de datos TeletexString** y **T61String** relacionados se codifican en 8 bits (o 16 bits para caracteres compuestos). Ambos tienen un número de etiqueta de 0x14. No se usan ampliamente.

## <a name="utf8string"></a>UTF8String

Etiqueta de codificación: 0x0C

Certreq.exe nombre: UTF8 \_ STRING

El formato de transformación UCS/Unicode de 8 bits (UTF-8) es una codificación de caracteres de longitud variable que puede representar cualquier carácter universal como un carácter Unicode, al tiempo que permite que los puntos de código iniciales sigan siendo coherentes con ASCII. UTF-8 usa de uno a cuatro bytes. El número de etiqueta es 0x0C.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




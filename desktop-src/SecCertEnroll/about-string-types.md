---
description: Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276806"
---
# <a name="string-types"></a>Tipos de cadena

Uno de los usos más comunes de las cadenas en una infraestructura de clave pública (PKI) es crear un nombre distintivo X. 500. Por ejemplo, el nombre de sujeto de una solicitud de certificado se crea mediante la combinación de una secuencia de nombres distintivos relativos, tal y como se muestra en el siguiente ejemplo de sintaxis.

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

La API de inscripción de certificados admite los siguientes tipos de cadena ASN. 1.

## <a name="bmpstring"></a>BMPString

Etiqueta de codificación: 0x1E

Nombre de Certreq.exe: cadena Unicode \_

El plano básico multilingüe (BMP) es una codificación de caracteres que engloba el primer plano del juego de caracteres universal (UCS). Hay diecisiete planos numerados de 0 a 16. BMP ocupa el plano 0 e incluye 65.536 puntos de código entre 0x0000 y 0xFFFF. Esta es la sección del mapa de caracteres Unicode, donde la mayoría de los caracteres asignados se han realizado hasta ahora. Incluye Latin, Oriente Medio, asiático, África y otros idiomas.

## <a name="ia5string"></a>IA5String

Etiqueta de codificación: 0x16

Nombre de Certreq.exe: IA5 \_ cadena

El alfabeto internacional número 5 (IA5) suele ser equivalente al alfabeto ASCII, pero las distintas versiones pueden incluir Acentos u otros caracteres específicos de un idioma regional. En el ejemplo siguiente se muestra el tipo **IA5String** que se usa en la definición de ASN. 1 de la extensión de certificado **AlternativeNames** .

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

Nombre de Certreq.exe: cadena IMPRIMIble \_

El tipo de datos **PrintableString** se diseñó originalmente para representar los juegos de caracteres limitados disponibles para los terminales de entrada de mainframe, pero se suele usar. Contiene los siguientes caracteres:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Etiqueta de codificación: 0x14

Los tipos de datos **TeletexString** y **T61String** relacionados se codifican en 8 bits (o 16 bits para caracteres compuestos). Ambos tienen un número de etiqueta de 0x14. No se usan exhaustivamente.

## <a name="utf8string"></a>UTF8String

Etiqueta de codificación: 0x0C

Nombre de la Certreq.exe: UTF8 \_ cadena

El formato de transformación UCS/Unicode (UTF-8) de 8 bits es una codificación de caracteres de longitud variable que puede representar cualquier carácter universal como carácter Unicode, al tiempo que permite que los puntos de código iniciales sigan siendo coherentes con ASCII. UTF-8 usa de uno a cuatro bytes. El número de etiqueta es 0x0C.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




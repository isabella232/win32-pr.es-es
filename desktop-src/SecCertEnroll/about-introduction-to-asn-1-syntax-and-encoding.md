---
description: La API de inscripción de certificados usa la notación de sintaxis abstracta uno (ASN. 1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introducción a la codificación y sintaxis de ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909649"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Introducción a la codificación y sintaxis de ASN. 1

La API de inscripción de certificados usa la notación de sintaxis abstracta uno (ASN. 1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación. ASN. 1 se puede dividir conceptualmente en un conjunto de reglas de sintaxis y un conjunto de reglas de codificación, tal y como se muestra en los ejemplos siguientes.

## <a name="asn1-syntax-example"></a>Ejemplo de sintaxis ASN. 1

Una solicitud de certificado contiene, entre otras cosas, el nombre de la entidad que realiza la solicitud o para la que se realiza la solicitud. El nombre es una secuencia de nombres distintivos relativos (RDN) de X. 500. Cada RDN de la secuencia consta de un identificador de objeto (OID) y un valor. En el ejemplo siguiente se muestra la sintaxis ASN. 1 para un nombre de sujeto.

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a>Ejemplo de codificación ASN. 1

La API de inscripción de certificados usa [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der) para codificar el nombre de sujeto anterior. DER requiere que cada elemento del nombre se represente mediante un tripledo TLV, donde T contiene el número de etiqueta del tipo ASN. 1, L contiene la longitud y V contiene el valor asociado. En el ejemplo siguiente se muestra cómo se codifica el nombre de sujeto TestCN. TestOrg.

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

Tenga en cuenta los siguientes puntos:

-   Línea 1:<dl> El nombre es una secuencia de nombres distintivos relativos.  
    El número de etiqueta del tipo de **secuencia** es 0x30.  
    El nombre de sujeto de TestCN. TestOrg requiere 35 (0x23) bytes.  
    </dl>
-   Line 2:<dl> El nombre común, TestCN, es un único conjunto de estructuras **AttributeTypeValue** .  
    El número de etiqueta de un **conjunto** es 0x31.  
    </dl>
-   Línea 3:<dl> La estructura **AttributeTypeValue** es una secuencia.  
    El número de etiqueta del tipo de **secuencia** es 0x30.  
    La estructura requiere 13 (0xD) bytes.  
    </dl>
-   Líneas 4 a 6:<dl> El identificador de objeto (OID) para el nombre común es 2.5.4.3.  
    El OID es un tipo de **\_ identificador de objeto** de tres bytes.  
    El número de etiqueta para el tipo de **\_ ID** . de objeto es 0x06.  
    </dl>
-   Líneas 7 a 9:<dl> El nombre común, TestCN, es un valor de cadena.  
    La cadena es un tipo de **\_ cadena imprimible** de seis bytes.  
    El número de etiqueta para el tipo de **\_ cadena imprimible** es 0x13.  
    </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación de solicitud de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 

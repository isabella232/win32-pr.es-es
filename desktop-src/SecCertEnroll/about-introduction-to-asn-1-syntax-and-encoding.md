---
description: La API de inscripción de certificados usa la notación de sintaxis abstracta One (ASN.1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introducción a la sintaxis y codificación de ASN.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504f6e643d91951351eaef2c51f9cfeac01919c77718a88ce866670f22803146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904234"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Introducción a la sintaxis y codificación de ASN.1

La API de inscripción de certificados usa la notación de sintaxis abstracta One (ASN.1) para definir, codificar y descodificar las solicitudes de certificado y los certificados que transfiere entre los equipos cliente y las entidades de certificación. ASN.1 se puede dividir conceptualmente en un conjunto de reglas de sintaxis y un conjunto de reglas de codificación, como se muestra en los ejemplos siguientes.

## <a name="asn1-syntax-example"></a>Ejemplo de sintaxis de ASN.1

Una solicitud de certificado contiene, entre otras cosas, el nombre de la entidad que realiza la solicitud o para la que se realiza la solicitud. El nombre es una secuencia de nombres distintivos relativos (RDN) X.500. Cada RDN de la secuencia consta de un identificador de objeto (OID) y un valor. La sintaxis ASN.1 para un nombre de sujeto se muestra en el ejemplo siguiente.

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

## <a name="asn1-encoding-example"></a>Ejemplo de codificación ASN.1

La API de inscripción de [*certificados reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (DER) para codificar el nombre de sujeto anterior. DER requiere que cada elemento del nombre se represente mediante un triplete TLV donde T contiene el número de etiqueta del tipo ASN.1, L contiene la longitud y V contiene el valor asociado. En el ejemplo siguiente se muestra cómo se codifica el nombre del sujeto TestCN.TestOrg.

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
    El número de etiqueta para **el tipo SEQUENCE** es 0x30.  
    El nombre de sujeto de TestCN.TestOrg requiere 35 bytes (0x23).  
    </dl>
-   Line 2:<dl> El nombre común, TestCN, es un único conjunto de **estructuras AttributeTypeValue.**  
    El número de etiqueta de **un set** es 0x31.  
    </dl>
-   Línea 3:<dl> La **estructura AttributeTypeValue** es una secuencia.  
    El número de etiqueta para **el tipo SEQUENCE** es 0x30.  
    La estructura requiere 13 bytes (0xD).  
    </dl>
-   Líneas 4 a 6:<dl> El identificador de objeto (OID) del nombre común es 2.5.4.3.  
    El OID es un tipo de id. **de objeto \_ de tres** bytes.  
    El número de etiqueta para el **tipo \_ de id. de** objeto es 0x06.  
    </dl>
-   Líneas 7 a 9:<dl> El nombre común, TestCN, es un valor de cadena.  
    La cadena es un tipo **DE CADENA IMPRIMIBLE \_ de seis** bytes.  
    El número de etiqueta para el **tipo CADENA \_ IMPRIMIBLE** es 0x13.  
    </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación de solicitud de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 

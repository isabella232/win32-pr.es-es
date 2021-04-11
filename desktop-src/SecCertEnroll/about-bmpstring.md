---
description: El tipo de datos ASN. 1 BMPString, denominado cadena Unicode \_ en la API de inscripción de certificados, se codifica en un triple TLV que comienza con un byte de etiqueta de 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c911218d852b792a333f015c825a7e4d1486b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276813"
---
# <a name="bmpstring"></a>BMPString

El tipo de datos ASN. 1 **BMPString** , denominado **\_ cadena UNIcode** en la API de inscripción de certificados, se codifica en un triple TLV que comienza con un byte de **etiqueta** de 0x1E. En el ejemplo siguiente, adaptado del tema de [ASN codificado de CMC. 1](cmc-encoded-asn-1.md) , se muestra la codificación de una extensión **TemplateName** . El nombre se puede especificar mediante la interfaz [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) . El identificador de objeto de la extensión es 1.3.6.1.4.1.311.13.2.1.

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

Si la cadena contiene menos de 128 bytes, el campo de **longitud** del trío TLV requiere un solo byte para especificar la longitud del contenido. Si la cadena tiene más de 127 bytes, el bit 7 del campo de **longitud** se establece en 1 y los bits 6 a 0 especifican el número de bytes adicionales que se usan para identificar la longitud del contenido. Para obtener más información, vea [longitud codificada y bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




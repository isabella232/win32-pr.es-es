---
description: El tipo de datos ASN.1 BMPString, denominado CADENA UNICODE en la API de inscripción de certificados, se codifica en un triplete TLV que comienza con un byte tag de \_ 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 496715d380739dd68dab4266422876ecca174b9caffd3895e9c465f446d32cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904844"
---
# <a name="bmpstring"></a>BMPString

El tipo de datos ASN.1 **BMPString,** denominado **\_ CADENA UNICODE** en la API de inscripción de certificados, se codifica en un triplete TLV que comienza con un **byte** tag de 0x1E. En el ejemplo siguiente, adaptado del tema [ASN.1](cmc-encoded-asn-1.md) codificado para CMC, se muestra la codificación de una **extensión TemplateName.** El nombre se puede especificar mediante la [**interfaz IX509ExtensionTemplateName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) El identificador de objeto de la extensión es 1.3.6.1.4.1.311.13.2.1.

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

Si la cadena contiene menos de 128 bytes, el campo **Longitud** del triplete TLV solo requiere un byte para especificar la longitud del contenido. Si la cadena tiene más de 127  bytes, el bit 7 del campo Longitud se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Para obtener más información, vea [Longitud codificada y Bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




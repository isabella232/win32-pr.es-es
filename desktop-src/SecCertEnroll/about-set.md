---
description: Set contiene una serie desordenada de campos de uno o varios tipos.
ms.assetid: 6bbe89da-1177-4cfa-9515-03b271e5ef6b
title: SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95eb2b9df8097f716ef98d55d052d2dbc2ef09b1bfe57de0e793d2b063967710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903684"
---
# <a name="set"></a>SET

Set **contiene** una serie desordenada de campos de uno o varios tipos. Se codifica en un triplete TLV que comienza con un byte **tag** de 0x31. En el ejemplo siguiente, adaptado del tema [ASN.1](cmc-encoded-asn-1.md) con codificación CMC, se muestra cómo se codifica un atributo **ClientId** en una estructura de datos **SET.** El atributo se puede especificar mediante la [**interfaz IX509AttributeClientId.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)

``` syntax
31 59                                     ; SET (59 Bytes)
   30 57                                  ; SEQUENCE (57 Bytes)
      06 09                               ; OBJECT_ID (9 Bytes)
      |  2b 06 01 04 01 82 37 15  14      ;   1.3.6.1.4.1.311.21.20 
      31 4a                               ; SET (4a Bytes)
         30 48                            ; SEQUENCE (48 Bytes)
            02 01                         ; INTEGER (1 Bytes)
            |  09
            0c 23                         ; UTF8_STRING (23 Bytes)
            |  76 69 63 68 33 64 2e 6a    ;   vich3d.j
            |  64 6f 6d 63 73 63 2e 6e    ;   domcsc.n
            |  74 74 65 73 74 2e 6d 69    ;   ttest.mi
            |  63 72 6f 73 6f 66 74 2e    ;   crosoft.
            |  63 6f 6d                   ;   com
            0c 15                         ; UTF8_STRING (15 Bytes)
            |  4a 44 4f 4d 43 53 43 5c    ;   JDOMCSC\
            |  61 64 6d 69 6e 69 73 74    ;   administ
            |  72 61 74 6f 72             ;   rator
            0c 07                         ; UTF8_STRING 
```

Si **set contiene** menos de 128 bytes, el campo **Longitud** del triplete TLV solo requiere un byte para especificar la longitud del contenido. Si tiene más de 127 bytes,  el bit 7 del campo Longitud se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Para obtener más información, vea [Longitud codificada y Bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




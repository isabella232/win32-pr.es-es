---
description: El tipo de datos BIT STRING se codifica en un triplete TLV que comienza con un byte tag de 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: CADENA DE BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056616a22cf2e683e943afef9369ed4c885963174aff0e72dea6ef718ddbdf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905070"
---
# <a name="bit-string"></a>CADENA DE BITS

El **tipo de datos BIT STRING** se codifica en un triplete TLV que comienza con un byte **tag** de 0x03. El **campo** Valor del triplete TLV contiene un byte inicial que especifica el número de bits que quedan sin usar en el byte final del contenido. En el ejemplo  siguiente, el campo Longitud se establece en 0x03 porque siguen  tres bytes de contenido y el byte inicial del campo Valor se establece en 0x04 porque hay cuatro bits sin usar en el último byte de contenido. Cada bit no utilizado se indica mediante la letra x.

![codificación der del tipo de datos de cadena de bits](images/der-tlv-bitstring.png)

En el ejemplo siguiente, adaptado del tema [PKCS \# 10 Encoded ASN.1,](pkcs--10-encoded-asn-1.md) se muestra la firma codificada de una solicitud de certificado PKCS \# 10 de ejemplo. El primer byte contiene el **valor tag** para el tipo de datos **BIT STRING,** 0x03. El segundo y tercer bytes contienen la longitud de la matriz de bytes. El bit 7 del segundo byte se establece en 1 porque hay más de 127 bytes de contenido. Los bits del 0 al 6 del segundo byte especifican el número de **bytes** de longitud final, en este caso uno. El tercer byte especifica el número de bytes de contenido, 0x81. El cuarto byte, 0x00, especifica el número de bits no usados que existen en el último byte de contenido. Tenga en cuenta que la firma está codificada en orden de bytes big-endian.

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Bytes de longitud y valor codificados](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




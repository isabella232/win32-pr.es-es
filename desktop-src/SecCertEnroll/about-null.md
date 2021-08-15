---
description: El valor NULL se codifica en un triplete TLV que comienza con un valor tag de 0x05, una longitud de 0x00 y ningún byte Value, como se muestra en la ilustración siguiente.
ms.assetid: f712f84a-c4d3-41bb-b151-62b0f86046af
title: "NULL"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be83b4e57640fdee783214186a8a2135f3d7d14325a4b3235f80d729ef4b6e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903817"
---
# <a name="null"></a>NULL

El **valor NULL** se codifica en un triplete TLV que comienza con  un valor **tag** de 0x05, una longitud de 0x00 y ningún byte **Value,** como se muestra en la ilustración siguiente.

![codificación der del tipo de datos NULL](images/der-tlv-null.png)

La quinta línea del ejemplo siguiente, adaptada del tema [PKCS \# 10 Encoded ASN.1,](pkcs--10-encoded-asn-1.md) muestra un valor **NULL** codificado. El primer byte es 0x05 y el segundo byte es 0x00. No hay ningún byte de contenido.

``` syntax
30 81 9f                                ; SEQUENCE (9f Bytes)
|  30 0d                                ; SEQUENCE (d Bytes)
|  |  06 09                             ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01  01    ; 1.2.840.113549.1.1.1
|  |  05 00                             ; NULL (0 Bytes)
|  03 81 8d                             ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                          ; SEQUENCE (89 Bytes)
|        02 81 81                       ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                          ; INTEGER (3 Bytes)
|           01 00 01
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




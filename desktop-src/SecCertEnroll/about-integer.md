---
description: Los valores enteros se codifican en un triplete TLV que comienza con un valor tag de 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEGER (API de inscripción de certificados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85151947653a66c98b7a030ade7b9ff7b4f5ee87fd84edc4cc52679be296a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904352"
---
# <a name="integer-certificate-enrollment-api"></a>INTEGER (API de inscripción de certificados)

Los valores enteros se codifican en un triplete TLV que comienza con **un valor tag** de 0x02. El **campo** Valor del triplete TLV contiene el entero codificado si es positivo o el complemento de sus dos si es negativo. Si el entero es positivo pero el bit de orden alto se establece en 1, se agrega un 0x00 inicial al contenido para indicar que el número no es negativo. Por ejemplo, el byte de orden superior de 0x8F (10001111) es 1. Por lo tanto, se agrega un byte cero inicial al contenido como se muestra en la ilustración siguiente.

![codificación der del tipo de datos booleano](images/der-tlv-integer.png)

Si el entero contiene menos de 128 bytes, el *campo Longitud* solo requiere un byte para especificar la longitud del contenido. Si el entero es superior a 127 bytes, el bit 7 del campo *Longitud* se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Para obtener más información, vea [Longitud codificada y Bytes de valor](about-encoded-length-and-value-bytes.md).

En el ejemplo siguiente, de [PKCS \# 10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), se muestra la codificación de una clave pública de 128 bytes. El primer byte contiene el **valor Tag** para el tipo de datos **INTEGER,** 0x02. El segundo y tercer bytes contienen el **valor Length.** El bit 7 del segundo byte se establece en 1 porque hay más de 127 bytes de contenido. Los bits del 0 al 6 del segundo byte especifican el número de bytes finales necesarios, en este caso uno, para especificar con precisión la longitud del contenido. El tercer byte especifica el número de bytes de contenido, 0x81. El cuarto byte, 0x00, se agrega al contenido para indicar que el entero es realmente un valor positivo aunque el bit de signo del byte de contenido inicial (0x8F) esté establecido en 1.

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

En el ejemplo siguiente se muestra cómo se codifica el 0x03 entero. El **byte** Tag contiene 0x02 y el byte **Length** especifica que hay un byte de contenido.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




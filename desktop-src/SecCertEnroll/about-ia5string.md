---
description: El tipo de datos ASN.1 IA5tring se codifica en un triplete TLV que comienza con un byte tag de 0x16.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5d602f50a7a3c22cd4a57d6531603307b9f14e02c537692c200a1b19fc361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904244"
---
# <a name="ia5string"></a>IA5String

El tipo de datos ASN.1 **IA5tring** se codifica en un triplete TLV que comienza con un byte **tag** de 0x16. En el ejemplo siguiente, adaptado del tema [ASN.1](cmc-encoded-asn-1.md) con codificación CMC, se muestra cómo se codifica el atributo **OSVersion** como un **tipo de IA5tring.** El número de versión se puede especificar mediante la [**interfaz IX509AttributeOSVersion.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) El identificador de objeto del atributo es 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Si la cadena contiene menos de 128 bytes, el campo **Longitud** del triplete TLV solo requiere un byte para especificar la longitud del contenido. Si la cadena tiene más de 127  bytes, el bit 7 del campo Longitud se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Para obtener más información, vea [Longitud codificada y Bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




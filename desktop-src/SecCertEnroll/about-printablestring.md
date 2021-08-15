---
description: El tipo de datos ASN.1 PrintableString se codifica en un triplete TLV que comienza con un byte tag de 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903764"
---
# <a name="printablestring"></a>PrintableString

El tipo de datos ASN.1 **PrintableString** se codifica en un triplete TLV que comienza con un byte **tag** de 0x13. En el ejemplo siguiente, del tema [PKCS \# 10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) , se muestra cómo se codifica un nombre común de usuario de TestCN como un tipo **PrintableString.** El identificador de objeto de un nombre común es 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Si la cadena contiene menos de 128 bytes, el campo **Longitud** del triplete TLV solo requiere un byte para especificar la longitud del contenido. Si la cadena tiene más de 127 bytes, el bit 7 del campo **Longitud** se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Para obtener más información, vea [Longitud codificada y Bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




---
description: El tipo de datos ASN. 1 PrintableString se codifica en un tripledo TLV que comienza con un byte de etiqueta de 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909642"
---
# <a name="printablestring"></a>PrintableString

El tipo de datos ASN. 1 **PrintableString** se codifica en un tripledo TLV que comienza con un byte de **etiqueta** de 0x13. En el ejemplo siguiente, del [tema \# ASN. 1 codificado de PKCS 10](pkcs--10-encoded-asn-1.md) , se muestra cómo un nombre común de usuario de TestCN se codifica como un tipo de **PrintableString** . El identificador de objeto de un nombre común es 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Si la cadena contiene menos de 128 bytes, el campo de **longitud** del trío TLV requiere un solo byte para especificar la longitud del contenido. Si la cadena tiene más de 127 bytes, el bit 7 del campo de **longitud** se establece en 1 y los bits 6 a 0 especifican el número de bytes adicionales que se usan para identificar la longitud del contenido. Para obtener más información, vea [longitud codificada y bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




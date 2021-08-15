---
description: El campo Etiqueta de un triplete TLV identifica el tipo de la estructura de datos que se envía entre equipos.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Bytes de etiqueta codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27face1fe04cf52c79d6c4047f87f58e98f2bc1a7b7656109341c9ce2be59d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904332"
---
# <a name="encoded-tag-bytes"></a>Bytes de etiqueta codificados

El *campo* Etiqueta de un triplete TLV identifica el tipo de la estructura de datos que se envía entre equipos. Por ejemplo, la etiqueta de un entero es 0x02 y la etiqueta de un identificador de objeto es 0x06. Aunque se permiten varios bytes, ninguno de los tipos de datos usados por la API de inscripción de certificados requiere más de uno. En la ilustración siguiente se muestra el desglose de un *valor de* etiqueta. Los bits 7 y 6 identifican la clase de etiquetado ASN.1. Hay cuatro clases disponibles, pero la API de inscripción de certificados usa tipos de datos que pertenecen solo a la clase UNIVERSAL. El bit 5 identifica si el formulario de codificación es primitivo o construido. Los tipos básicos y de cadena se codifican mediante formularios primitivos, tipos construidos mediante un formulario construido. Para obtener más información, [vea ASN.1 Type System](about-asn-1-type-system.md). Los bits del 4 al 0 contienen el número de etiqueta.

![der tlv tag byte](images/der-tlv-tagbyte.png)

En la tabla siguiente se enumeran los tipos de datos admitidos por la API de inscripción de certificados, el formulario de codificación utilizado y el valor de etiqueta.

| Tipo              | ASN.1 (clase) | Formulario de codificación | Valor de etiqueta                             |
|-------------------|-------------|---------------|---------------------------------------|
| CADENA DE BITS        | Universal   | Primitivo     | 00000011<br/> (0x03)<br/> |
| BOOLEAN           | Universal   | Primitivo     | 00000001<br/> (0x01)<br/> |
| INTEGER           | Universal   | Primitivo     | 00000010<br/> (0x02)<br/> |
| NULL              | Universal   | Primitivo     | 00000101<br/> (0x05)<br/> |
| IDENTIFICADOR DE OBJETO | Universal   | Primitivo     | 00000110<br/> (0x06)<br/> |
| OCTET STRING      | Universal   | Primitivo     | 00000100<br/> (0x04)<br/> |
| BMPString         | Universal   | Primitivo     | 00011110<br/> (0x1E)<br/> |
| IA5String         | Universal   | Primitivo     | 00010110<br/> (0x16)<br/> |
| PrintableString   | Universal   | Primitivo     | 00010011<br/> (0x13)<br/> |
| TeletexString     | Universal   | Primitivo     | 00010100<br/> (0x14)<br/> |
| UTF8String        | Universal   | Primitivo     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | Universal   | Construido   | 00110000<br/> (0x30)<br/> |
| SEQUENCE OF       | Universal   | Construido   | 00110000<br/> (0x30)<br/> |
| SET               | Universal   | Construido   | 00110001<br/> (0x31)<br/> |
| SET OF            | Universal   | Construido   | 00110001<br/> (0x31)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de transferencia de DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de longitud y valor codificados](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 





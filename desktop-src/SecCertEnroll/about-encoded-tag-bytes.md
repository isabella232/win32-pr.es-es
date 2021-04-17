---
description: El campo etiqueta de un trío TLV identifica el tipo de la estructura de datos que se envía entre equipos.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Bytes de etiqueta codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567358"
---
# <a name="encoded-tag-bytes"></a>Bytes de etiqueta codificados

El campo *etiqueta* de un trío TLV identifica el tipo de la estructura de datos que se envía entre equipos. Por ejemplo, la etiqueta de un entero es 0x02 y la etiqueta de un identificador de objeto es 0x06. Aunque se permiten varios bytes, ninguno de los tipos de datos utilizados por la API de inscripción de certificados requiere más de uno. En la ilustración siguiente se muestra el desglose de un valor de *etiqueta* . Los bits 7 y 6 identifican la clase de etiquetado ASN. 1. Hay cuatro clases disponibles, pero la API de inscripción de certificados usa tipos de datos que solo pertenecen a la clase UNIVERSAL. Bit 5 identifica si el formato de codificación es primitivo o construido. Los tipos básicos y de cadena se codifican utilizando formas primitivas, tipos construidos con un formato construido. Para obtener más información, consulte [sistema de tipos ASN. 1](about-asn-1-type-system.md). Los bits 4 a 0 contienen el número de etiqueta.

![byte de etiqueta der TLV](images/der-tlv-tagbyte.png)

En la tabla siguiente se enumeran los tipos de datos admitidos por la API de inscripción de certificados, el formato de codificación utilizado y el valor de etiqueta.

| Tipo              | Clase ASN. 1 | Formulario de codificación | Valor de etiqueta                             |
|-------------------|-------------|---------------|---------------------------------------|
| CADENA DE BITS        | MUNDO   | Primitivo     | 00000011<br/> 0x03<br/> |
| BOOLEAN           | MUNDO   | Primitivo     | 00000001<br/> 0x01<br/> |
| INTEGER           | MUNDO   | Primitivo     | 00000010<br/> 0x02<br/> |
| NULL              | MUNDO   | Primitivo     | 00000101<br/> 0x05<br/> |
| IDENTIFICADOR DE OBJETO | MUNDO   | Primitivo     | 00000110<br/> 0x06<br/> |
| CADENA DE OCTETO      | MUNDO   | Primitivo     | 00000100<br/> 0x04<br/> |
| BMPString         | MUNDO   | Primitivo     | 00011110<br/> STOP<br/> |
| IA5String         | MUNDO   | Primitivo     | 00010110<br/> (0x16)<br/> |
| PrintableString   | MUNDO   | Primitivo     | 00010011<br/> 0x13 ó<br/> |
| TeletexString     | MUNDO   | Primitivo     | 00010100<br/> 0x14<br/> |
| UTF8String        | MUNDO   | Primitivo     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | MUNDO   | Construido   | 00110000<br/> 0x30<br/> |
| SECUENCIA DE       | MUNDO   | Construido   | 00110000<br/> 0x30<br/> |
| SET               | MUNDO   | Construido   | 00110001<br/> 0x31<br/> |
| CONJUNTO DE            | MUNDO   | Construido   | 00110001<br/> 0x31<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de transferencia DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de valor y longitud codificados](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 





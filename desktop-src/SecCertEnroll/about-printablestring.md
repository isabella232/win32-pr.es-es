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
# <a name="printablestring"></a><span data-ttu-id="dfa9d-103">PrintableString</span><span class="sxs-lookup"><span data-stu-id="dfa9d-103">PrintableString</span></span>

<span data-ttu-id="dfa9d-104">El tipo de datos ASN. 1 **PrintableString** se codifica en un tripledo TLV que comienza con un byte de **etiqueta** de 0x13.</span><span class="sxs-lookup"><span data-stu-id="dfa9d-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="dfa9d-105">En el ejemplo siguiente, del [tema \# ASN. 1 codificado de PKCS 10](pkcs--10-encoded-asn-1.md) , se muestra cómo un nombre común de usuario de TestCN se codifica como un tipo de **PrintableString** .</span><span class="sxs-lookup"><span data-stu-id="dfa9d-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="dfa9d-106">El identificador de objeto de un nombre común es 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="dfa9d-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="dfa9d-107">Si la cadena contiene menos de 128 bytes, el campo de **longitud** del trío TLV requiere un solo byte para especificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="dfa9d-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="dfa9d-108">Si la cadena tiene más de 127 bytes, el bit 7 del campo de **longitud** se establece en 1 y los bits 6 a 0 especifican el número de bytes adicionales que se usan para identificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="dfa9d-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="dfa9d-109">Para obtener más información, vea [longitud codificada y bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="dfa9d-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfa9d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfa9d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfa9d-111">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="dfa9d-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="dfa9d-112">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="dfa9d-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




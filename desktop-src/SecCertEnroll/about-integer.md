---
description: Los valores enteros se codifican en un tripledo TLV que comienza con un valor de etiqueta de 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: ENTERO (API de inscripción de certificados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360686"
---
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="ac0e8-103">ENTERO (API de inscripción de certificados)</span><span class="sxs-lookup"><span data-stu-id="ac0e8-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="ac0e8-104">Los valores enteros se codifican en un tripledo TLV que comienza con un valor de **etiqueta** de 0x02.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="ac0e8-105">El campo de **valor** del trío TLV contiene el entero codificado si es positivo, o el complemento de sus dos si es negativo.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="ac0e8-106">Si el entero es positivo pero el bit de orden superior se establece en 1, se agrega a la izquierda una 0x00 al contenido para indicar que el número no es negativo.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="ac0e8-107">Por ejemplo, el byte de orden superior de 0x8F (10001111) es 1.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="ac0e8-108">Por lo tanto, se agrega un byte de cero a la izquierda al contenido tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![codificación der del tipo de datos Boolean](images/der-tlv-integer.png)

<span data-ttu-id="ac0e8-110">Si el entero contiene menos de 128 bytes, el campo de *longitud* requiere un solo byte para especificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="ac0e8-111">Si el entero es superior a 127 bytes, el bit 7 del campo de *longitud* se establece en 1 y los bits 6 a 0 especifican el número de bytes adicionales que se usan para identificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="ac0e8-112">Para obtener más información, vea [longitud codificada y bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="ac0e8-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="ac0e8-113">En el ejemplo siguiente, [de \# ASN. 1 con codificación PKCS 10](pkcs--10-encoded-asn-1.md), se muestra la codificación de una clave pública de 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="ac0e8-114">El primer byte contiene el valor de **etiqueta** para el tipo de datos **Integer** , 0x02.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="ac0e8-115">El segundo y tercer bytes contienen el valor de **longitud** .</span><span class="sxs-lookup"><span data-stu-id="ac0e8-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="ac0e8-116">El bit 7 del segundo byte se establece en 1 porque hay más de 127 bytes de contenido.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="ac0e8-117">Los bits del 0 al 6 del segundo byte especifican el número de bytes finales necesarios, en este caso uno, para especificar con precisión la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="ac0e8-118">El tercer byte especifica el número de bytes de contenido, 0x81.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="ac0e8-119">El cuarto byte, 0x00, se agrega al contenido para indicar que el entero es realmente un valor positivo aunque el bit de signo del byte de contenido inicial (0x8F) se establezca en 1.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

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

<span data-ttu-id="ac0e8-120">En el ejemplo siguiente se muestra cómo se codifica el valor entero 0x03.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="ac0e8-121">El byte de **etiqueta** contiene 0x02 y el byte de **longitud** especifica que hay un byte de contenido.</span><span class="sxs-lookup"><span data-stu-id="ac0e8-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="ac0e8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac0e8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac0e8-123">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ac0e8-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="ac0e8-124">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="ac0e8-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 




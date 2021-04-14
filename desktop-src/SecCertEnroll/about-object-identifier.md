---
description: El tipo de datos del identificador de objeto se codifica en un tripledo TLV que comienza con un valor de etiqueta de 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICADOR DE OBJETO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276810"
---
# <a name="object-identifier"></a><span data-ttu-id="38a84-103">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="38a84-103">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="38a84-104">El tipo de datos del **identificador de objeto** se codifica en un tripledo TLV que comienza con un valor de **etiqueta** de 0x06.</span><span class="sxs-lookup"><span data-stu-id="38a84-104">The **OBJECT IDENTIFIER** data type is encoded into a TLV triplet that begins with a **Tag** value of 0x06.</span></span> <span data-ttu-id="38a84-105">Cada entero de un identificador de objeto decimal con puntos (OID) se codifica según las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="38a84-105">Each integer of a dotted decimal object identifier (OID) is encoded according to the following rules:</span></span>

-   <span data-ttu-id="38a84-106">Los dos primeros nodos del OID se codifican en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="38a84-106">The first two nodes of the OID are encoded onto a single byte.</span></span> <span data-ttu-id="38a84-107">El primer nodo se multiplica por el decimal 40 y el resultado se agrega al valor del segundo nodo.</span><span class="sxs-lookup"><span data-stu-id="38a84-107">The first node is multiplied by the decimal 40 and the result is added to the value of the second node.</span></span>
-   <span data-ttu-id="38a84-108">Los valores de nodo menores o iguales a 127 se codifican en un byte.</span><span class="sxs-lookup"><span data-stu-id="38a84-108">Node values less than or equal to 127 are encoded on one byte.</span></span>
-   <span data-ttu-id="38a84-109">Los valores de nodo mayores o iguales que 128 se codifican en varios bytes.</span><span class="sxs-lookup"><span data-stu-id="38a84-109">Node values greater than or equal to 128 are encoded on multiple bytes.</span></span> <span data-ttu-id="38a84-110">El bit 7 del byte situado más a la izquierda se establece en uno.</span><span class="sxs-lookup"><span data-stu-id="38a84-110">Bit 7 of the leftmost byte is set to one.</span></span> <span data-ttu-id="38a84-111">Los bits del 0 al 6 de cada byte contienen el valor codificado.</span><span class="sxs-lookup"><span data-stu-id="38a84-111">Bits 0 through 6 of each byte contains the encoded value.</span></span>

<span data-ttu-id="38a84-112">Estos puntos se muestran en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="38a84-112">These points are shown by the following illustration.</span></span>

![codificación der del tipo de datos del identificador de objeto](images/der-tlv-oid.png)

<span data-ttu-id="38a84-114">En el ejemplo siguiente se muestra cómo el atributo **ClientID** se codifica en una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="38a84-114">The following example shows how the **ClientId** attribute is encoded in a certificate request.</span></span>

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 




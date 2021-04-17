---
description: El campo de longitud de un trío TLV identifica el número de bytes codificados en el campo de valor.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Bytes de valor y longitud codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666951"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="19e41-103">Bytes de valor y longitud codificados</span><span class="sxs-lookup"><span data-stu-id="19e41-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="19e41-104">El campo de *longitud* de un trío TLV identifica el número de bytes codificados en el campo de *valor* .</span><span class="sxs-lookup"><span data-stu-id="19e41-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="19e41-105">El campo *valor* contiene el contenido que se envía entre equipos.</span><span class="sxs-lookup"><span data-stu-id="19e41-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="19e41-106">Si el campo de *valor* contiene menos de 128 bytes, el campo de *longitud* solo requiere un byte.</span><span class="sxs-lookup"><span data-stu-id="19e41-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="19e41-107">El bit 7 del campo de *longitud* es cero (0) y los bits restantes identifican el número de bytes de contenido que se envía.</span><span class="sxs-lookup"><span data-stu-id="19e41-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="19e41-108">Si el campo de *valor* contiene más de 127 bytes, el bit 7 del campo de *longitud* es uno (1) y los bits restantes identifican el número de bytes necesarios para contener la longitud.</span><span class="sxs-lookup"><span data-stu-id="19e41-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="19e41-109">Los ejemplos se muestran en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="19e41-109">Examples are shown in the following illustration.</span></span>

![byte de longitud del TLV der](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="19e41-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19e41-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e41-112">Sintaxis de transferencia DER</span><span class="sxs-lookup"><span data-stu-id="19e41-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="19e41-113">Bytes de etiqueta codificados</span><span class="sxs-lookup"><span data-stu-id="19e41-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 




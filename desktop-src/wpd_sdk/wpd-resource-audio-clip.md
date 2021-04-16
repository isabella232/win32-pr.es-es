---
description: Especifica un clip de audio para el objeto.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678289"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="6d3ab-103">\_clip de \_ audio de recursos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="6d3ab-104">Especifica un clip de audio para el objeto.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="6d3ab-105">Este tipo de recurso debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="6d3ab-106">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="6d3ab-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="6d3ab-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="6d3ab-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="6d3ab-108">velocidad de bits de \_ audio WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="6d3ab-109">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="6d3ab-110">recuento de canales de audio de WPD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="6d3ab-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-111">Optional.</span></span>                                              |
| [<span data-ttu-id="6d3ab-112">\_código de \_ formato de audio de WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="6d3ab-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-113">Optional.</span></span>                                              |
| [<span data-ttu-id="6d3ab-114">\_profundidad de \_ bits de audio de WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="6d3ab-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-115">Optional.</span></span>                                              |
| [<span data-ttu-id="6d3ab-116">\_alineación del \_ bloque de audio de WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="6d3ab-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-117">Optional.</span></span>                                              |
| [<span data-ttu-id="6d3ab-118">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="6d3ab-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-119">Required.</span></span>                                              |
| [<span data-ttu-id="6d3ab-120">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="6d3ab-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="6d3ab-121">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="6d3ab-122">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="6d3ab-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="6d3ab-123">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="6d3ab-124">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="6d3ab-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="6d3ab-125">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="6d3ab-126">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="6d3ab-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="6d3ab-127">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="6d3ab-128">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="6d3ab-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="6d3ab-129">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="6d3ab-130">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="6d3ab-131">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-131">Required.</span></span>                                              |
| [<span data-ttu-id="6d3ab-132">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d3ab-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="6d3ab-133">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="6d3ab-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d3ab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3ab-135">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="6d3ab-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




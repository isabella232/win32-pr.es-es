---
description: Especifica una imagen pequeña&\# 8212; normalmente una versión más pequeña de una imagen más grande en el objeto.
ms.assetid: ad1eac9d-b182-49b2-bd2c-2d76e2026d80
title: WPD_RESOURCE_THUMBNAIL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc26af624f756f55ccb10ccf3f8c7bf3e6a6035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154160"
---
# <a name="wpd_resource_thumbnail"></a><span data-ttu-id="aa531-103">\_miniatura de recursos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="aa531-103">WPD\_RESOURCE\_THUMBNAIL</span></span>

<span data-ttu-id="aa531-104">Especifica una imagen pequeña, normalmente una versión más pequeña de una imagen más grande en el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa531-104">Specifies a small picture—typically a smaller version of a larger picture in the object.</span></span>

<span data-ttu-id="aa531-105">Este tipo de recurso debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="aa531-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="aa531-106">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="aa531-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="aa531-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="aa531-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="aa531-108">\_ancho de medios de WPD \_</span><span class="sxs-lookup"><span data-stu-id="aa531-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="aa531-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa531-109">Required.</span></span>                                              |
| [<span data-ttu-id="aa531-110">altura de los medios de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="aa531-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="aa531-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa531-111">Required.</span></span>                                              |
| [<span data-ttu-id="aa531-112">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="aa531-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="aa531-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa531-113">Required.</span></span>                                              |
| [<span data-ttu-id="aa531-114">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="aa531-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="aa531-115">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="aa531-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="aa531-116">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="aa531-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="aa531-117">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="aa531-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="aa531-118">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="aa531-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="aa531-119">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="aa531-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="aa531-120">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="aa531-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="aa531-121">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="aa531-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="aa531-122">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="aa531-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="aa531-123">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="aa531-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="aa531-124">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="aa531-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="aa531-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa531-125">Required.</span></span>                                              |
| [<span data-ttu-id="aa531-126">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="aa531-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="aa531-127">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="aa531-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="aa531-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa531-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa531-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="aa531-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




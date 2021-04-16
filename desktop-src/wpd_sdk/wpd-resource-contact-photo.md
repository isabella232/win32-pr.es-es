---
description: Especifica una imagen que representa una fotografía de la persona a la que se hace referencia en el objeto de contacto.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705525"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="baf33-103">\_foto de \_ contacto de recursos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="baf33-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="baf33-104">Especifica una imagen que representa una fotografía de la persona a la que se hace referencia en el objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="baf33-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="baf33-105">Este tipo de recurso debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="baf33-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="baf33-106">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="baf33-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="baf33-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="baf33-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="baf33-108">\_ancho de medios de WPD \_</span><span class="sxs-lookup"><span data-stu-id="baf33-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="baf33-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf33-109">Required.</span></span>                                              |
| [<span data-ttu-id="baf33-110">altura de los medios de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="baf33-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="baf33-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf33-111">Required.</span></span>                                              |
| [<span data-ttu-id="baf33-112">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="baf33-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="baf33-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf33-113">Required.</span></span>                                              |
| [<span data-ttu-id="baf33-114">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="baf33-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="baf33-115">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="baf33-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="baf33-116">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="baf33-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="baf33-117">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="baf33-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="baf33-118">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="baf33-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="baf33-119">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="baf33-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="baf33-120">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="baf33-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="baf33-121">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="baf33-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="baf33-122">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="baf33-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="baf33-123">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="baf33-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="baf33-124">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="baf33-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="baf33-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf33-125">Required.</span></span>                                              |
| [<span data-ttu-id="baf33-126">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="baf33-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="baf33-127">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="baf33-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="baf33-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="baf33-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf33-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="baf33-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




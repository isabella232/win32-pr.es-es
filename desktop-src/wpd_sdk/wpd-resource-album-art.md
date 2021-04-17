---
description: Especifica una imagen que representa la ilustración del álbum para el objeto.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541230"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="04003-103">\_carátula de \_ álbum de recursos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="04003-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="04003-104">Especifica una imagen que representa la ilustración del álbum para el objeto.</span><span class="sxs-lookup"><span data-stu-id="04003-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="04003-105">Este tipo de recurso debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="04003-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="04003-106">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="04003-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="04003-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="04003-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="04003-108">\_ancho de medios de WPD \_</span><span class="sxs-lookup"><span data-stu-id="04003-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="04003-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04003-109">Required.</span></span>                                              |
| [<span data-ttu-id="04003-110">altura de los medios de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="04003-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="04003-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04003-111">Required.</span></span>                                              |
| [<span data-ttu-id="04003-112">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="04003-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="04003-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04003-113">Required.</span></span>                                              |
| [<span data-ttu-id="04003-114">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="04003-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="04003-115">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="04003-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="04003-116">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="04003-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="04003-117">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="04003-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="04003-118">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="04003-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="04003-119">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="04003-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="04003-120">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="04003-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="04003-121">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="04003-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="04003-122">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="04003-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="04003-123">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="04003-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="04003-124">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="04003-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="04003-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04003-125">Required.</span></span>                                              |
| [<span data-ttu-id="04003-126">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="04003-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="04003-127">Recomendado</span><span class="sxs-lookup"><span data-stu-id="04003-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="04003-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04003-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04003-129">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="04003-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




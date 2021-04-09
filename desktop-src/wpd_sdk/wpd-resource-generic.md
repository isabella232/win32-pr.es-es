---
description: Especifica un tipo de recurso que no se define de otro modo en dispositivos portátiles de Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154161"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="53317-103">\_recursos genéricos del recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="53317-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="53317-104">Especifica un tipo de recurso que no se define de otro modo en dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="53317-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="53317-105">Puede definir sus propios recursos personalizados que admitan cualquier atributo personalizado o dispositivos portátiles definidos por Windows.</span><span class="sxs-lookup"><span data-stu-id="53317-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="53317-106">Sin embargo, cualquier recurso que cree debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="53317-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="53317-107">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="53317-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="53317-108">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="53317-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="53317-109">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="53317-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="53317-110">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53317-110">Required.</span></span>                                              |
| [<span data-ttu-id="53317-111">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="53317-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="53317-112">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="53317-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="53317-113">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="53317-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="53317-114">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="53317-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="53317-115">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="53317-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="53317-116">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="53317-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="53317-117">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="53317-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="53317-118">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="53317-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="53317-119">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="53317-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="53317-120">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="53317-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="53317-121">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="53317-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="53317-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53317-122">Required.</span></span>                                              |
| [<span data-ttu-id="53317-123">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="53317-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="53317-124">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="53317-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="53317-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="53317-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53317-126">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="53317-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




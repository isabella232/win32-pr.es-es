---
description: '\_grupo de \_ contactos de tipo de contenido de WPD \_ \_'
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278302"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="d05af-103">\_grupo de \_ contactos de tipo de contenido de WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="d05af-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="d05af-104">Un objeto que describe su tipo como tipo \_ de contenido de WPD el \_ \_ \_ grupo de contactos representa un grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="d05af-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="d05af-105">Las referencias del objeto WPD de este objeto \_ \_ contienen una lista de identificadores de objeto para los distintos objetos de contacto del tipo de contenido de WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d05af-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="d05af-106">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d05af-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="d05af-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d05af-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="d05af-108">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="d05af-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d05af-109">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d05af-110">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d05af-110">Required.</span></span>                                                             |
| [<span data-ttu-id="d05af-111">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d05af-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d05af-112">Required.</span></span>                                                             |
| [<span data-ttu-id="d05af-113">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d05af-114">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="d05af-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d05af-115">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d05af-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d05af-116">Required.</span></span>                                                             |
| [<span data-ttu-id="d05af-117">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d05af-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d05af-118">Required.</span></span>                                                             |
| [<span data-ttu-id="d05af-119">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d05af-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d05af-120">Required.</span></span>                                                             |
| [<span data-ttu-id="d05af-121">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="d05af-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d05af-122">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="d05af-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="d05af-123">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="d05af-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d05af-124">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="d05af-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="d05af-125">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d05af-126">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="d05af-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="d05af-127">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d05af-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d05af-128">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="d05af-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d05af-129">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="d05af-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d05af-130">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d05af-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="d05af-131">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d05af-132">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="d05af-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="d05af-133">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d05af-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="d05af-135">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d05af-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="d05af-137">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="d05af-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d05af-138">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="d05af-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="d05af-139">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="d05af-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d05af-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="d05af-141">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="d05af-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d05af-142">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="d05af-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="d05af-143">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="d05af-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d05af-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="d05af-145">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="d05af-146">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="d05af-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="d05af-147">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d05af-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d05af-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="d05af-149">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="d05af-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d05af-150">Opcionales</span><span class="sxs-lookup"><span data-stu-id="d05af-150">Optional</span></span>                                                              |
| [<span data-ttu-id="d05af-151">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="d05af-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="d05af-152">Obligatorio si el objeto se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="d05af-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="d05af-153">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="d05af-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d05af-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d05af-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="d05af-155">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="d05af-155">Typical Resources</span></span>

<span data-ttu-id="d05af-156">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d05af-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d05af-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d05af-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d05af-158">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="d05af-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




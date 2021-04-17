---
description: '\_calendario de \_ tipo de contenido de WPD \_'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706863"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="e7d66-103">\_calendario de \_ tipo de contenido de WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="e7d66-104">Objeto que describe su tipo como calendario de \_ tipo de contenido de WPD \_ \_ representa un calendario.</span><span class="sxs-lookup"><span data-stu-id="e7d66-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="e7d66-105">El objeto puede ser un archivo que contiene información de calendario o una carpeta que contiene otros objetos relacionados con el calendario, como tareas, citas, etc.</span><span class="sxs-lookup"><span data-stu-id="e7d66-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="e7d66-106">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7d66-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="e7d66-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="e7d66-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="e7d66-108">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="e7d66-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e7d66-109">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="e7d66-110">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7d66-110">Required.</span></span>                                                             |
| [<span data-ttu-id="e7d66-111">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="e7d66-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7d66-112">Required.</span></span>                                                             |
| [<span data-ttu-id="e7d66-113">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="e7d66-114">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d66-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="e7d66-115">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="e7d66-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7d66-116">Required.</span></span>                                                             |
| [<span data-ttu-id="e7d66-117">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="e7d66-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7d66-118">Required.</span></span>                                                             |
| [<span data-ttu-id="e7d66-119">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="e7d66-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7d66-120">Required.</span></span>                                                             |
| [<span data-ttu-id="e7d66-121">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="e7d66-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="e7d66-122">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="e7d66-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="e7d66-123">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="e7d66-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="e7d66-124">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="e7d66-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="e7d66-125">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="e7d66-126">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="e7d66-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="e7d66-127">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e7d66-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="e7d66-128">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d66-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="e7d66-129">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="e7d66-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="e7d66-130">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7d66-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="e7d66-131">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="e7d66-132">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="e7d66-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="e7d66-133">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="e7d66-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-135">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="e7d66-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-137">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="e7d66-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="e7d66-138">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="e7d66-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="e7d66-139">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="e7d66-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="e7d66-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-141">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="e7d66-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="e7d66-142">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="e7d66-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="e7d66-143">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="e7d66-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="e7d66-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-145">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="e7d66-146">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="e7d66-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="e7d66-147">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e7d66-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="e7d66-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-149">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="e7d66-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="e7d66-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="e7d66-151">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="e7d66-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="e7d66-152">Obligatorio si el objeto se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="e7d66-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="e7d66-153">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="e7d66-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="e7d66-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7d66-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="e7d66-155">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="e7d66-155">Typical Resources</span></span>

<span data-ttu-id="e7d66-156">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="e7d66-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="e7d66-157">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="e7d66-157">Resource Name</span></span>                                          | <span data-ttu-id="e7d66-158">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="e7d66-158">Required or Optional</span></span>                             | <span data-ttu-id="e7d66-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7d66-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="e7d66-160">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7d66-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="e7d66-161">Obligatorio si el objeto está respaldado por datos binarios.</span><span class="sxs-lookup"><span data-stu-id="e7d66-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="e7d66-162">Contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="e7d66-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e7d66-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d66-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d66-164">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="e7d66-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




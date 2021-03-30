---
description: '\_programa de \_ tipo de contenido de WPD \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816275"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="69462-103">\_programa de \_ tipo de contenido de WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="69462-104">Objeto que describe su tipo como el tipo de contenido de WPD que \_ \_ \_ representa un programa ejecutable.</span><span class="sxs-lookup"><span data-stu-id="69462-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="69462-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="69462-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69462-106">**Nombre de la propiedad**</span><span class="sxs-lookup"><span data-stu-id="69462-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="69462-107">**Obligatorio u opcional**</span><span class="sxs-lookup"><span data-stu-id="69462-107">**Required or Optional**</span></span>                                                           |
| [<span data-ttu-id="69462-108">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="69462-109">Obligatorio, pero de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69462-109">Required, but read-only.</span></span> <span data-ttu-id="69462-110">Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="69462-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="69462-111">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="69462-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69462-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="69462-113">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="69462-114">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="69462-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="69462-115">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="69462-116">Requerido, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69462-116">Required, read-only.</span></span> <span data-ttu-id="69462-117">Un cliente no puede establecer esta propiedad incluso en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="69462-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="69462-118">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="69462-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69462-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="69462-120">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="69462-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69462-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="69462-122">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="69462-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="69462-123">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="69462-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="69462-124">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="69462-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="69462-125">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="69462-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="69462-126">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="69462-127">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="69462-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="69462-128">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="69462-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="69462-129">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="69462-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="69462-130">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="69462-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="69462-131">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69462-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="69462-132">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="69462-133">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="69462-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="69462-134">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="69462-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-136">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="69462-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-138">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="69462-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="69462-139">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="69462-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="69462-140">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="69462-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="69462-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-142">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="69462-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="69462-143">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="69462-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="69462-144">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="69462-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="69462-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-146">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="69462-147">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="69462-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="69462-148">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="69462-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="69462-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-150">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="69462-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="69462-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="69462-152">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="69462-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="69462-153">Es obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="69462-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="69462-154">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="69462-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="69462-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69462-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="69462-156">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="69462-156">Typical Resources</span></span>

<span data-ttu-id="69462-157">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="69462-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="69462-158">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="69462-158">Resource Name</span></span>                                          | <span data-ttu-id="69462-159">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="69462-159">Required or Optional</span></span> | <span data-ttu-id="69462-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="69462-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="69462-161">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="69462-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="69462-162">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69462-162">Required.</span></span>            | <span data-ttu-id="69462-163">Contiene el archivo de programa.</span><span class="sxs-lookup"><span data-stu-id="69462-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="69462-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69462-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69462-165">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="69462-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




---
description: PROGRAMA DE TIPO \_ DE \_ CONTENIDO \_ WPD
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423775"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="e5e9f-103">PROGRAMA DE TIPO \_ DE \_ CONTENIDO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="e5e9f-104">Un objeto que describe su tipo como WPD \_ CONTENT TYPE PROGRAM representa un programa \_ \_ ejecutable.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="e5e9f-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="e5e9f-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="e5e9f-106">Property Name</span></span>     | <span data-ttu-id="e5e9f-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="e5e9f-107">Required or Optional</span></span>      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5e9f-108">IDENTIFICADOR DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="e5e9f-109">Obligatorio, pero de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-109">Required, but read-only.</span></span> <span data-ttu-id="e5e9f-110">Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="e5e9f-111">IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="e5e9f-112">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-113">NOMBRE DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="e5e9f-114">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="e5e9f-115">IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="e5e9f-116">Obligatorio, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-116">Required, read-only.</span></span> <span data-ttu-id="e5e9f-117">Un cliente no puede establecer esta propiedad ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="e5e9f-118">FORMATO DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="e5e9f-119">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-120">TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="e5e9f-121">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-122">\_ISHIDDEN DEL \_ OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="e5e9f-123">Obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="e5e9f-124">ISSYSTEM DEL \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="e5e9f-125">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="e5e9f-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="e5e9f-126">TAMAÑO DEL OBJETO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="e5e9f-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="e5e9f-127">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="e5e9f-128">NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="e5e9f-129">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="e5e9f-130">OBJETO WPD \_ \_ NO \_ CONSUMIBLE</span><span class="sxs-lookup"><span data-stu-id="e5e9f-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="e5e9f-131">Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="e5e9f-132">REFERENCIAS DE OBJETOS \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="e5e9f-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="e5e9f-133">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="e5e9f-134">PALABRAS CLAVE DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="e5e9f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-136">IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="e5e9f-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-138">EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="e5e9f-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="e5e9f-139">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="e5e9f-140">FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_</span><span class="sxs-lookup"><span data-stu-id="e5e9f-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="e5e9f-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-142">FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="e5e9f-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="e5e9f-143">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="e5e9f-144">FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="e5e9f-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-146">REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5e9f-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="e5e9f-147">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="e5e9f-148">IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="e5e9f-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-150">WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE</span><span class="sxs-lookup"><span data-stu-id="e5e9f-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="e5e9f-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="e5e9f-152">EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR</span><span class="sxs-lookup"><span data-stu-id="e5e9f-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="e5e9f-153">Obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="e5e9f-154">CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="e5e9f-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="e5e9f-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="e5e9f-156">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="e5e9f-156">Typical Resources</span></span>

<span data-ttu-id="e5e9f-157">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="e5e9f-158">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="e5e9f-158">Resource Name</span></span>                                          | <span data-ttu-id="e5e9f-159">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="e5e9f-159">Required or Optional</span></span> | <span data-ttu-id="e5e9f-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e9f-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="e5e9f-161">**WPD \_ RESOURCE \_ DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e5e9f-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="e5e9f-162">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-162">Required.</span></span>            | <span data-ttu-id="e5e9f-163">Contiene el archivo de programa.</span><span class="sxs-lookup"><span data-stu-id="e5e9f-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5e9f-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5e9f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5e9f-165">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="e5e9f-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




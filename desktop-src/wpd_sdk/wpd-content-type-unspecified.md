---
description: TIPO DE \_ CONTENIDO \_ WPD \_ SIN ESPECIFICAR
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423685"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="cd115-103">TIPO DE \_ CONTENIDO \_ WPD \_ SIN ESPECIFICAR</span><span class="sxs-lookup"><span data-stu-id="cd115-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="cd115-104">Un objeto que describe su tipo como WPD CONTENT TYPE UNSPECIFIED representa un objeto genérico que puede o \_ no tener un archivo físico \_ \_ subyacente.</span><span class="sxs-lookup"><span data-stu-id="cd115-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="cd115-105">La diferencia entre este tipo y WPD CONTENT TYPE GENERIC FILE es que los objetos \_ \_ \_ \_ \_ WPD CONTENT \_ TYPE GENERIC FILE deben tener un archivo físico \_ \_ subyacente.</span><span class="sxs-lookup"><span data-stu-id="cd115-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="cd115-106">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd115-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="cd115-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="cd115-107">Property Name</span></span>       | <span data-ttu-id="cd115-108">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="cd115-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="cd115-109">IDENTIFICADOR DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="cd115-110">Obligatorio, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd115-110">Required, read-only.</span></span> <span data-ttu-id="cd115-111">Un cliente no puede establecer esta propiedad ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="cd115-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="cd115-112">IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="cd115-113">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cd115-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="cd115-114">NOMBRE DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="cd115-115">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd115-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="cd115-116">IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="cd115-117">Obligatorio, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd115-117">Required, read-only.</span></span> <span data-ttu-id="cd115-118">Un cliente no puede establecer esta propiedad ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="cd115-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="cd115-119">FORMATO DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="cd115-120">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cd115-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="cd115-121">TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="cd115-122">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cd115-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="cd115-123">\_ISHIDDEN DEL \_ OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="cd115-124">Obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="cd115-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="cd115-125">WPD \_ OBJECT \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="cd115-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="cd115-126">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="cd115-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="cd115-127">TAMAÑO DEL OBJETO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="cd115-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="cd115-128">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="cd115-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="cd115-129">NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="cd115-130">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd115-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="cd115-131">OBJETO WPD \_ \_ NO \_ CONSUMIBLE</span><span class="sxs-lookup"><span data-stu-id="cd115-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="cd115-132">Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd115-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="cd115-133">REFERENCIAS DE OBJETOS \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="cd115-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="cd115-134">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="cd115-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="cd115-135">PALABRAS CLAVE DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="cd115-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-137">IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="cd115-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-139">EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="cd115-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="cd115-140">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="cd115-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="cd115-141">FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_</span><span class="sxs-lookup"><span data-stu-id="cd115-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="cd115-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-143">FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="cd115-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="cd115-144">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="cd115-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="cd115-145">FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="cd115-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-147">REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="cd115-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="cd115-148">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="cd115-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="cd115-149">IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="cd115-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-151">OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO</span><span class="sxs-lookup"><span data-stu-id="cd115-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="cd115-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="cd115-153">EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR</span><span class="sxs-lookup"><span data-stu-id="cd115-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="cd115-154">Obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cd115-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="cd115-155">CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="cd115-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="cd115-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd115-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="cd115-157">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="cd115-157">Typical Resources</span></span>

<span data-ttu-id="cd115-158">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="cd115-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="cd115-159">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="cd115-159">Resource Name</span></span>                                          | <span data-ttu-id="cd115-160">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="cd115-160">Required or Optional</span></span>                             | <span data-ttu-id="cd115-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd115-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="cd115-162">**WPD \_ RESOURCE \_ DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd115-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="cd115-163">Obligatorio si el objeto está respaldo de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="cd115-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="cd115-164">Contiene los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="cd115-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cd115-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd115-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd115-166">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="cd115-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




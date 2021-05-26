---
description: PERFIL INALÁMBRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423705"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="40a8f-103">PERFIL INALÁMBRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="40a8f-104">Un objeto que describe su tipo como WPD CONTENT TYPE WIRELESS PROFILE representa \_ la información utilizada para acceder a una red \_ \_ \_ inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="40a8f-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="40a8f-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="40a8f-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="40a8f-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="40a8f-106">Property Name</span></span>             | <span data-ttu-id="40a8f-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="40a8f-107">Required or Optional</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="40a8f-108">IDENTIFICADOR DE OBJETO \_ DE \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="40a8f-109">Necesario.</span><span class="sxs-lookup"><span data-stu-id="40a8f-109">Required.</span></span>                                                             |
| [<span data-ttu-id="40a8f-110">IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="40a8f-111">Necesario.</span><span class="sxs-lookup"><span data-stu-id="40a8f-111">Required.</span></span>                                                             |
| [<span data-ttu-id="40a8f-112">NOMBRE DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="40a8f-113">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="40a8f-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="40a8f-114">WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID</span><span class="sxs-lookup"><span data-stu-id="40a8f-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="40a8f-115">Necesario.</span><span class="sxs-lookup"><span data-stu-id="40a8f-115">Required.</span></span>                                                             |
| [<span data-ttu-id="40a8f-116">FORMATO DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="40a8f-117">Necesario.</span><span class="sxs-lookup"><span data-stu-id="40a8f-117">Required.</span></span>                                                             |
| [<span data-ttu-id="40a8f-118">TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="40a8f-119">Necesario.</span><span class="sxs-lookup"><span data-stu-id="40a8f-119">Required.</span></span>                                                             |
| [<span data-ttu-id="40a8f-120">\_ISHIDDEN DEL \_ OBJETO WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="40a8f-121">Obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="40a8f-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="40a8f-122">WPD \_ OBJECT \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="40a8f-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="40a8f-123">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="40a8f-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="40a8f-124">TAMAÑO DEL OBJETO \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="40a8f-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="40a8f-125">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="40a8f-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="40a8f-126">NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="40a8f-127">Obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="40a8f-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="40a8f-128">OBJETO WPD \_ \_ NO \_ CONSUMIBLE</span><span class="sxs-lookup"><span data-stu-id="40a8f-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="40a8f-129">Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40a8f-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="40a8f-130">REFERENCIAS A OBJETOS \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="40a8f-131">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="40a8f-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="40a8f-132">PALABRAS CLAVE DE \_ OBJETO \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="40a8f-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-134">IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="40a8f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-136">EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM</span><span class="sxs-lookup"><span data-stu-id="40a8f-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="40a8f-137">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="40a8f-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="40a8f-138">FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="40a8f-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-140">FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="40a8f-141">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="40a8f-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="40a8f-142">FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="40a8f-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-144">REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="40a8f-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="40a8f-145">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="40a8f-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="40a8f-146">IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="40a8f-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-148">OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO</span><span class="sxs-lookup"><span data-stu-id="40a8f-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="40a8f-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="40a8f-150">EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR</span><span class="sxs-lookup"><span data-stu-id="40a8f-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="40a8f-151">Obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="40a8f-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="40a8f-152">CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD</span><span class="sxs-lookup"><span data-stu-id="40a8f-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="40a8f-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40a8f-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="40a8f-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="40a8f-154">Typical Resources</span></span>

<span data-ttu-id="40a8f-155">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="40a8f-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="40a8f-156">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="40a8f-156">Resource Name</span></span>                                          | <span data-ttu-id="40a8f-157">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="40a8f-157">Required or Optional</span></span>                                  | <span data-ttu-id="40a8f-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="40a8f-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="40a8f-159">**WPD \_ RESOURCE \_ DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="40a8f-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="40a8f-160">Obligatorio si el objeto está representado por datos binarios.</span><span class="sxs-lookup"><span data-stu-id="40a8f-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="40a8f-161">Contiene los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="40a8f-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="40a8f-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40a8f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a8f-163">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="40a8f-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




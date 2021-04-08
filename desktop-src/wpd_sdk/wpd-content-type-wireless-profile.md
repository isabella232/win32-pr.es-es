---
description: '\_ \_ perfil inalámbrico de tipo de contenido de \_ WPD \_'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a327efa9e1a4cd3a1e5927da89ae4f9e7092196a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002616"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="b9355-103">\_ \_ perfil inalámbrico de tipo de contenido de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="b9355-104">Objeto que describe su tipo como el tipo de contenido de WPD el \_ \_ \_ \_ perfil inalámbrico representa la información que se usa para tener acceso a una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="b9355-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="b9355-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9355-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b9355-106">**Nombre de la propiedad**</span><span class="sxs-lookup"><span data-stu-id="b9355-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="b9355-107">**Obligatorio u opcional**</span><span class="sxs-lookup"><span data-stu-id="b9355-107">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="b9355-108">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="b9355-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9355-109">Required.</span></span>                                                             |
| [<span data-ttu-id="b9355-110">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="b9355-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9355-111">Required.</span></span>                                                             |
| [<span data-ttu-id="b9355-112">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="b9355-113">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="b9355-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="b9355-114">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="b9355-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9355-115">Required.</span></span>                                                             |
| [<span data-ttu-id="b9355-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="b9355-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9355-117">Required.</span></span>                                                             |
| [<span data-ttu-id="b9355-118">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="b9355-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9355-119">Required.</span></span>                                                             |
| [<span data-ttu-id="b9355-120">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="b9355-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="b9355-121">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="b9355-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="b9355-122">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="b9355-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="b9355-123">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="b9355-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="b9355-124">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="b9355-125">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="b9355-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="b9355-126">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="b9355-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="b9355-127">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="b9355-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="b9355-128">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="b9355-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="b9355-129">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9355-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="b9355-130">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="b9355-131">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="b9355-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="b9355-132">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="b9355-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-134">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="b9355-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-136">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="b9355-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="b9355-137">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="b9355-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="b9355-138">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="b9355-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="b9355-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-140">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="b9355-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="b9355-141">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="b9355-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="b9355-142">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="b9355-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="b9355-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-144">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="b9355-145">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="b9355-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="b9355-146">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="b9355-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="b9355-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-148">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="b9355-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="b9355-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="b9355-150">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="b9355-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="b9355-151">Es obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="b9355-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="b9355-152">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="b9355-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="b9355-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9355-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="b9355-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="b9355-154">Typical Resources</span></span>

<span data-ttu-id="b9355-155">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="b9355-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="b9355-156">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="b9355-156">Resource Name</span></span>                                          | <span data-ttu-id="b9355-157">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="b9355-157">Required or Optional</span></span>                                  | <span data-ttu-id="b9355-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9355-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="b9355-159">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b9355-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="b9355-160">Obligatorio si el objeto se representa mediante datos binarios.</span><span class="sxs-lookup"><span data-stu-id="b9355-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="b9355-161">Contiene los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="b9355-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b9355-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9355-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9355-163">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="b9355-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




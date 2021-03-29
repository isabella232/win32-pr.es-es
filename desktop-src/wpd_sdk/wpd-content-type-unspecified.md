---
description: tipo de contenido de WPD no \_ \_ \_ especificado
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b767ba2d76dc569def42b80eb646ae0e6a6aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912130"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="4c2c3-103">tipo de contenido de WPD no \_ \_ \_ especificado</span><span class="sxs-lookup"><span data-stu-id="4c2c3-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="4c2c3-104">Un objeto que describe su tipo como tipo de contenido de WPD \_ \_ \_ no especificado representa un objeto genérico que puede tener o no un archivo físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="4c2c3-105">La diferencia entre este tipo y el \_ archivo genérico de tipo de contenido de WPD \_ \_ \_ es que los \_ objetos de archivo genérico de tipo de contenido de WPD \_ \_ \_ deben tener un archivo físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="4c2c3-106">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-106">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="4c2c3-107">**Nombre de la propiedad**</span><span class="sxs-lookup"><span data-stu-id="4c2c3-107">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="4c2c3-108">**Obligatorio u opcional**</span><span class="sxs-lookup"><span data-stu-id="4c2c3-108">**Required or Optional**</span></span>                                                      |
| [<span data-ttu-id="4c2c3-109">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="4c2c3-110">Requerido, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-110">Required, read-only.</span></span> <span data-ttu-id="4c2c3-111">Un cliente no puede establecer esta propiedad incluso en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="4c2c3-112">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="4c2c3-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-114">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="4c2c3-115">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="4c2c3-116">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="4c2c3-117">Requerido, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-117">Required, read-only.</span></span> <span data-ttu-id="4c2c3-118">Un cliente no puede establecer esta propiedad incluso en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="4c2c3-119">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="4c2c3-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-121">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="4c2c3-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-123">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="4c2c3-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="4c2c3-124">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="4c2c3-125">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="4c2c3-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="4c2c3-126">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="4c2c3-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="4c2c3-127">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="4c2c3-128">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="4c2c3-129">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="4c2c3-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="4c2c3-130">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="4c2c3-131">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="4c2c3-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="4c2c3-132">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="4c2c3-133">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="4c2c3-134">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="4c2c3-135">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="4c2c3-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-137">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="4c2c3-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-139">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="4c2c3-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="4c2c3-140">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="4c2c3-141">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="4c2c3-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="4c2c3-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-143">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="4c2c3-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="4c2c3-144">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="4c2c3-145">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="4c2c3-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="4c2c3-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-147">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="4c2c3-148">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="4c2c3-149">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="4c2c3-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="4c2c3-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-151">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="4c2c3-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="4c2c3-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="4c2c3-153">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="4c2c3-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="4c2c3-154">Es obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="4c2c3-155">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="4c2c3-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="4c2c3-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="4c2c3-157">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="4c2c3-157">Typical Resources</span></span>

<span data-ttu-id="4c2c3-158">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="4c2c3-159">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="4c2c3-159">Resource Name</span></span>                                          | <span data-ttu-id="4c2c3-160">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="4c2c3-160">Required or Optional</span></span>                             | <span data-ttu-id="4c2c3-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c2c3-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="4c2c3-162">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="4c2c3-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="4c2c3-163">Obligatorio si el objeto está respaldado por datos binarios.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="4c2c3-164">Contiene los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="4c2c3-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4c2c3-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c2c3-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c2c3-166">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="4c2c3-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




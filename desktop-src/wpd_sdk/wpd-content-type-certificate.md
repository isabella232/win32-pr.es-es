---
description: '\_certificado de \_ tipo de contenido de WPD \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706862"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="c23cd-103">\_certificado de \_ tipo de contenido de WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="c23cd-104">Un objeto que describe su tipo como \_ certificado de tipo de contenido de WPD \_ \_ representa un certificado utilizado para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c23cd-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="c23cd-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="c23cd-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="c23cd-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="c23cd-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="c23cd-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="c23cd-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c23cd-108">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="c23cd-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-109">Required.</span></span>                                                             |
| [<span data-ttu-id="c23cd-110">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="c23cd-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-111">Required.</span></span>                                                             |
| [<span data-ttu-id="c23cd-112">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="c23cd-113">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="c23cd-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="c23cd-114">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="c23cd-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-115">Required.</span></span>                                                             |
| [<span data-ttu-id="c23cd-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="c23cd-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-117">Required.</span></span>                                                             |
| [<span data-ttu-id="c23cd-118">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="c23cd-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-119">Required.</span></span>                                                             |
| [<span data-ttu-id="c23cd-120">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="c23cd-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="c23cd-121">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="c23cd-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="c23cd-122">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="c23cd-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="c23cd-123">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="c23cd-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="c23cd-124">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="c23cd-125">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="c23cd-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="c23cd-126">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c23cd-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="c23cd-127">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="c23cd-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="c23cd-128">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="c23cd-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="c23cd-129">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c23cd-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="c23cd-130">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="c23cd-131">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="c23cd-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="c23cd-132">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="c23cd-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-134">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="c23cd-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-136">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="c23cd-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="c23cd-137">Obligatorio si el objeto está protegido por la tecnología DRM.</span><span class="sxs-lookup"><span data-stu-id="c23cd-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="c23cd-138">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="c23cd-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="c23cd-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-140">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="c23cd-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="c23cd-141">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="c23cd-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="c23cd-142">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="c23cd-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="c23cd-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-144">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="c23cd-145">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="c23cd-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="c23cd-146">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="c23cd-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="c23cd-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-148">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="c23cd-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="c23cd-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="c23cd-150">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="c23cd-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="c23cd-151">Obligatorio si el objeto se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="c23cd-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="c23cd-152">\_ \_ configuración regional de idioma del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="c23cd-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="c23cd-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c23cd-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="c23cd-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="c23cd-154">Typical Resources</span></span>

<span data-ttu-id="c23cd-155">Estos objetos suelen incluir los siguientes recursos.</span><span class="sxs-lookup"><span data-stu-id="c23cd-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="c23cd-156">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="c23cd-156">Resource Name</span></span>                                          | <span data-ttu-id="c23cd-157">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="c23cd-157">Required or Optional</span></span> | <span data-ttu-id="c23cd-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="c23cd-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="c23cd-159">**\_valor predeterminado del recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c23cd-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="c23cd-160">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c23cd-160">Required.</span></span>            | <span data-ttu-id="c23cd-161">Contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="c23cd-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c23cd-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c23cd-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c23cd-163">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="c23cd-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




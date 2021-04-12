---
description: Objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ televisor representa una grabación de televisión.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361075"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="a394c-103">\_ \_ televisor tipo de contenido de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="a394c-104">Objeto que describe su tipo como tipo de contenido de WPD el \_ \_ \_ televisor representa una grabación de televisión.</span><span class="sxs-lookup"><span data-stu-id="a394c-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="a394c-105">Este tipo de objeto debe hospedar las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="a394c-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="a394c-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a394c-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="a394c-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="a394c-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a394c-108">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="a394c-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a394c-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="a394c-110">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="a394c-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a394c-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="a394c-112">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="a394c-113">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="a394c-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="a394c-114">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="a394c-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a394c-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="a394c-116">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="a394c-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a394c-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="a394c-118">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="a394c-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a394c-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="a394c-120">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="a394c-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="a394c-121">Es obligatorio si el objeto está oculto.</span><span class="sxs-lookup"><span data-stu-id="a394c-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="a394c-122">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="a394c-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="a394c-123">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="a394c-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="a394c-124">\_tamaño del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="a394c-125">Obligatorio si el objeto tiene al menos un recurso.</span><span class="sxs-lookup"><span data-stu-id="a394c-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="a394c-126">\_nombre de \_ \_ archivo original del objeto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a394c-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="a394c-127">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="a394c-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="a394c-128">\_objeto WPD \_ no \_ consumible</span><span class="sxs-lookup"><span data-stu-id="a394c-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="a394c-129">Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a394c-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="a394c-130">\_referencias a objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="a394c-131">Obligatorio si el objeto tiene referencias a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="a394c-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="a394c-132">\_palabras clave del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="a394c-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-134">\_identificador de \_ sincronización del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="a394c-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-136">el \_ objeto \_ WPD \_ está \_ protegido con DRM</span><span class="sxs-lookup"><span data-stu-id="a394c-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="a394c-137">Obligatorio si el objeto está protegido por la tecnología de Rights Management digital.</span><span class="sxs-lookup"><span data-stu-id="a394c-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="a394c-138">\_fecha de objeto WPD \_ \_ creada</span><span class="sxs-lookup"><span data-stu-id="a394c-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="a394c-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-140">\_fecha del objeto WPD \_ \_ modificada</span><span class="sxs-lookup"><span data-stu-id="a394c-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="a394c-141">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="a394c-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="a394c-142">\_fecha del objeto WPD \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="a394c-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="a394c-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-144">\_ \_ referencias inversas de objetos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a394c-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="a394c-145">Se recomienda si otro objeto hace referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="a394c-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="a394c-146">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a394c-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="a394c-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-148">\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a394c-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="a394c-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-150">el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso</span><span class="sxs-lookup"><span data-stu-id="a394c-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="a394c-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a394c-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a394c-152">el \_ objeto WPD \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="a394c-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="a394c-153">Es obligatorio si no se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="a394c-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="a394c-154">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="a394c-154">Typical Resources</span></span>

<span data-ttu-id="a394c-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a394c-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="a394c-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a394c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a394c-157">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="a394c-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




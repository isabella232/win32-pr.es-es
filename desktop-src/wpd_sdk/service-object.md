---
description: Objeto de servicio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913289"
---
# <a name="service-object"></a><span data-ttu-id="18d3e-103">Objeto de servicio</span><span class="sxs-lookup"><span data-stu-id="18d3e-103">Service Object</span></span>

<span data-ttu-id="18d3e-104">El objeto de servicio debe admitir las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="18d3e-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="18d3e-105">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="18d3e-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="18d3e-106">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="18d3e-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18d3e-107">[\_identificador de objeto de WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="18d3e-108">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-108">Required.</span></span> <span data-ttu-id="18d3e-109">.</span><span class="sxs-lookup"><span data-stu-id="18d3e-109">.</span></span>                                                                           |
| <span data-ttu-id="18d3e-110">[\_ \_ ID. primario del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="18d3e-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-111">Required.</span></span>                                                                             |
| <span data-ttu-id="18d3e-112">[\_nombre del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="18d3e-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-113">Required.</span></span>                                                                             |
| <span data-ttu-id="18d3e-114">[\_ \_ \_ identificador único persistente del objeto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="18d3e-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-115">Required.</span></span>                                                                             |
| <span data-ttu-id="18d3e-116">[\_objeto WPD \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="18d3e-117">Obligatorio si el objeto de servicio no se debe mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="18d3e-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="18d3e-118">[\_objeto WPD \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="18d3e-119">Obligatorio si el objeto es un objeto del sistema (por ejemplo, representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="18d3e-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="18d3e-120">[\_categoría de \_ objeto \_ funcional de WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="18d3e-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-121">Required.</span></span> <span data-ttu-id="18d3e-122">Representa el tipo de servicio de dispositivo, como los contactos de servicio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="18d3e-123">[\_versión del servicio WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="18d3e-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-124">Required.</span></span>                                                                             |
| <span data-ttu-id="18d3e-125">[\_tipo de almacenamiento de WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="18d3e-126">Obligatorio si el servicio se utiliza para almacenar objetos.</span><span class="sxs-lookup"><span data-stu-id="18d3e-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="18d3e-127">[\_capacidad de almacenamiento de WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18d3e-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="18d3e-128">Obligatorio si el servicio se utiliza para almacenar objetos.</span><span class="sxs-lookup"><span data-stu-id="18d3e-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="18d3e-129">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="18d3e-129">Typical Resources</span></span>

<span data-ttu-id="18d3e-130">Normalmente, estos objetos no hospedan recursos.</span><span class="sxs-lookup"><span data-stu-id="18d3e-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="18d3e-131">Formatos típicos</span><span class="sxs-lookup"><span data-stu-id="18d3e-131">Typical Formats</span></span>

<span data-ttu-id="18d3e-132">En la siguiente lista se identifican los formatos típicos utilizados por el objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="18d3e-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="18d3e-133">Sin embargo, este objeto no se limita a estos formatos.</span><span class="sxs-lookup"><span data-stu-id="18d3e-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="18d3e-134">formato de objeto WPD no \_ \_ \_ especificado</span><span class="sxs-lookup"><span data-stu-id="18d3e-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="18d3e-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18d3e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d3e-136">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="18d3e-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 

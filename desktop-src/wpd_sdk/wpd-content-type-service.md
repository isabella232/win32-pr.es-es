---
description: '\_servicio de \_ tipo de contenido de WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002617"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="93cee-103">\_servicio de \_ tipo de contenido de WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="93cee-104">Objeto que describe su tipo como servicio de \_ tipo de contenido WPD \_ \_ representa un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93cee-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="93cee-105">Este tipo de objeto admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="93cee-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="93cee-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="93cee-106">Property Name</span></span>                                                                                        | <span data-ttu-id="93cee-107">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="93cee-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="93cee-108">\_identificador de objeto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="93cee-109">Requerido, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93cee-109">Required, read-only.</span></span> <span data-ttu-id="93cee-110">Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="93cee-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="93cee-111">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="93cee-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93cee-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="93cee-113">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="93cee-114">Es obligatorio si el objeto representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="93cee-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="93cee-115">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="93cee-116">Requerido, de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93cee-116">Required, read-only.</span></span> <span data-ttu-id="93cee-117">Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="93cee-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="93cee-118">\_objeto WPD \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="93cee-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="93cee-119">Obligatorio si el servicio no se debe mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="93cee-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="93cee-120">\_objeto WPD \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="93cee-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="93cee-121">Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).</span><span class="sxs-lookup"><span data-stu-id="93cee-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="93cee-122">\_categoría de \_ objeto \_ funcional de WPD</span><span class="sxs-lookup"><span data-stu-id="93cee-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="93cee-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93cee-123">Required.</span></span> <span data-ttu-id="93cee-124">Representa el tipo de servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93cee-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="93cee-125">\_versión del servicio WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="93cee-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93cee-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="93cee-127">\_tipo de almacenamiento de WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="93cee-128">Obligatorio si el servicio se utiliza para almacenar objetos.</span><span class="sxs-lookup"><span data-stu-id="93cee-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="93cee-129">\_capacidad de almacenamiento de WPD \_</span><span class="sxs-lookup"><span data-stu-id="93cee-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="93cee-130">Obligatorio si el servicio se utiliza para almacenar objetos.</span><span class="sxs-lookup"><span data-stu-id="93cee-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="93cee-131">Recursos típicos</span><span class="sxs-lookup"><span data-stu-id="93cee-131">Typical Resources</span></span>

<span data-ttu-id="93cee-132">Estos objetos no hospedan recursos.</span><span class="sxs-lookup"><span data-stu-id="93cee-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93cee-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93cee-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93cee-134">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="93cee-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




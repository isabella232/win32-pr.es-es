---
description: Especifica el archivo completo detrás del objeto. También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están incluidos en otros tipos de recursos de dispositivos portátiles de Windows, como un tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546547"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="149e6-104">\_valor predeterminado del recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="149e6-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="149e6-105">Especifica el archivo completo detrás del objeto.</span><span class="sxs-lookup"><span data-stu-id="149e6-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="149e6-106">También es una manera de hacer referencia a cualquier tipo de recurso, incluidos los que no están incluidos en otros tipos de recursos de dispositivos portátiles de Windows, como un tipo de objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="149e6-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="149e6-107">Se incluirán todos los recursos insertados en el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="149e6-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="149e6-108">Por ejemplo, el recurso predeterminado de una carpeta raíz de contactos puede incluir todos los contactos anidados.</span><span class="sxs-lookup"><span data-stu-id="149e6-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="149e6-109">Sin embargo, no se incluyen los recursos secundarios que simplemente están *vinculados* por metadatos o referencias.</span><span class="sxs-lookup"><span data-stu-id="149e6-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="149e6-110">Un ejemplo de esto sería una lista de reproducción, que solo podría vincularse a archivos de audio a través de referencias de metadatos o referencias de ruta de texto en el archivo.</span><span class="sxs-lookup"><span data-stu-id="149e6-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="149e6-111">El único valor de *PID* permitido para esta **PROPERTYKEY** es cero.</span><span class="sxs-lookup"><span data-stu-id="149e6-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="149e6-112">Este tipo de recurso debe admitir los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="149e6-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="149e6-113">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="149e6-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="149e6-114">Obligatorio u opcional</span><span class="sxs-lookup"><span data-stu-id="149e6-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="149e6-115">\_ \_ Tamaño total del atributo de recursos de \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="149e6-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="149e6-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="149e6-116">Required.</span></span>                                              |
| [<span data-ttu-id="149e6-117">el \_ atributo del recurso WPD \_ \_ puede \_ leer</span><span class="sxs-lookup"><span data-stu-id="149e6-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="149e6-118">Obligatorio si los clientes pueden leer este recurso.</span><span class="sxs-lookup"><span data-stu-id="149e6-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="149e6-119">el \_ atributo del recurso WPD \_ \_ puede \_ escribir</span><span class="sxs-lookup"><span data-stu-id="149e6-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="149e6-120">Obligatorio si los clientes pueden escribir en este recurso.</span><span class="sxs-lookup"><span data-stu-id="149e6-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="149e6-121">el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="149e6-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="149e6-122">Obligatorio si los clientes pueden eliminar este recurso.</span><span class="sxs-lookup"><span data-stu-id="149e6-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="149e6-123">\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="149e6-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="149e6-124">Obligatorio si los clientes tienen acceso de lectura al recurso.</span><span class="sxs-lookup"><span data-stu-id="149e6-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="149e6-125">\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD</span><span class="sxs-lookup"><span data-stu-id="149e6-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="149e6-126">Obligatorio si los clientes tienen acceso de escritura al recurso.</span><span class="sxs-lookup"><span data-stu-id="149e6-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="149e6-127">\_formato de \_ atributo de recurso de WPD \_</span><span class="sxs-lookup"><span data-stu-id="149e6-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="149e6-128">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="149e6-128">Required.</span></span>                                              |
| [<span data-ttu-id="149e6-129">\_clave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="149e6-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="149e6-130">Se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="149e6-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="149e6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="149e6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149e6-132">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="149e6-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 




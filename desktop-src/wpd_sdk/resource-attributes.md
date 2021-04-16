---
description: Los dispositivos portátiles de Windows admiten los siguientes atributos de recursos.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Atributos de recursos (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718952"
---
# <a name="resource-attributes"></a><span data-ttu-id="cbf9a-103">Atributos de recursos</span><span class="sxs-lookup"><span data-stu-id="cbf9a-103">Resource Attributes</span></span>

<span data-ttu-id="cbf9a-104">Los dispositivos portátiles de Windows admiten los siguientes atributos de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="cbf9a-105">Estos atributos se devuelven mediante los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf9a-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="cbf9a-106">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="cbf9a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="cbf9a-107">Attribute</span></span>                                                  | <span data-ttu-id="cbf9a-108">VarType</span><span class="sxs-lookup"><span data-stu-id="cbf9a-108">VarType</span></span>      | <span data-ttu-id="cbf9a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf9a-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf9a-110">**el \_ atributo de recurso de WPD \_ \_ puede \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="cbf9a-111">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-111">**VT\_BOOL**</span></span> | <span data-ttu-id="cbf9a-112">Valor booleano que especifica si un cliente tiene permiso para eliminar el recurso.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="cbf9a-113">Si no está presente, se supone que es false.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="cbf9a-114">**el \_ atributo del recurso WPD \_ \_ puede \_ leer**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="cbf9a-115">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-115">**VT\_BOOL**</span></span> | <span data-ttu-id="cbf9a-116">Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="cbf9a-117">Si no está presente, se supone que es false.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="cbf9a-118">**el \_ atributo del recurso WPD \_ \_ puede \_ escribir**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="cbf9a-119">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-119">**VT\_BOOL**</span></span> | <span data-ttu-id="cbf9a-120">Valor booleano que especifica si un cliente tiene permiso para abrir el recurso para el acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="cbf9a-121">Si no está presente, se supone que es false.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="cbf9a-122">**\_tamaño de \_ \_ búfer de \_ lectura óptimo del \_ atributo \_ de recurso de WPD**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="cbf9a-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-123">**VT\_UI4**</span></span>  | <span data-ttu-id="cbf9a-124">Tamaño de búfer recomendado que un llamador debe utilizar para las lecturas almacenadas en búfer del recurso.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="cbf9a-125">**\_tamaño de \_ \_ búfer de \_ escritura óptimo del \_ atributo \_ de recurso de WPD**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="cbf9a-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-126">**VT\_UI4**</span></span>  | <span data-ttu-id="cbf9a-127">Tamaño de búfer recomendado que un llamador debe utilizar para las escrituras almacenadas en búfer en el recurso.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="cbf9a-128">**\_ \_ Tamaño total del atributo de recursos de \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="cbf9a-129">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-129">**VT\_UI8**</span></span>  | <span data-ttu-id="cbf9a-130">Tamaño total de los datos de recursos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf9a-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="cbf9a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbf9a-131">Requirements</span></span>



| <span data-ttu-id="cbf9a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf9a-132">Requirement</span></span> | <span data-ttu-id="cbf9a-133">Value</span><span class="sxs-lookup"><span data-stu-id="cbf9a-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf9a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbf9a-134">Header</span></span><br/> | <dl> <span data-ttu-id="cbf9a-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf9a-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf9a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbf9a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf9a-137">**Propiedades**</span><span class="sxs-lookup"><span data-stu-id="cbf9a-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





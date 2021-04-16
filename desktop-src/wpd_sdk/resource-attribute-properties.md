---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propiedades de los atributos de recursos (PortableDevice. h)
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
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718953"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="d702b-103">Propiedades de atributo de recurso</span><span class="sxs-lookup"><span data-stu-id="d702b-103">Resource Attribute Properties</span></span>

<span data-ttu-id="d702b-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de atributo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d702b-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="d702b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d702b-105">Property</span></span>                                    | <span data-ttu-id="d702b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d702b-106">VarType</span></span>         | <span data-ttu-id="d702b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d702b-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d702b-108">**\_clave de \_ recurso de atributo de recurso WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d702b-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="d702b-109">**VT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="d702b-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="d702b-110">Se trata de un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contiene un valor único, que es la clave que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="d702b-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="d702b-111">**\_formato de \_ atributo de recurso de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d702b-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="d702b-112">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="d702b-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="d702b-113">Valor GUID que especifica el formato del recurso.</span><span class="sxs-lookup"><span data-stu-id="d702b-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="d702b-114">Vea [formatos de objeto](object-format-guids.md) para obtener una lista de formatos definidos por dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="d702b-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="d702b-115">**\_ \_ Tamaño total del atributo de recursos de \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d702b-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="d702b-116">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="d702b-116">**VT\_UI8**</span></span>     | <span data-ttu-id="d702b-117">Tamaño total de los datos de recursos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d702b-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d702b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d702b-118">Remarks</span></span>

<span data-ttu-id="d702b-119">Estos atributos son devueltos por el método [**IPortableDeviceResources:: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="d702b-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d702b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d702b-120">Requirements</span></span>



| <span data-ttu-id="d702b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d702b-121">Requirement</span></span> | <span data-ttu-id="d702b-122">Value</span><span class="sxs-lookup"><span data-stu-id="d702b-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d702b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d702b-123">Header</span></span><br/> | <dl> <span data-ttu-id="d702b-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d702b-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d702b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d702b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d702b-126">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="d702b-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="d702b-127">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="d702b-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





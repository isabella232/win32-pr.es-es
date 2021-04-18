---
description: Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697217"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="ddcd2-104">Elemento PnPXDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="ddcd2-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="ddcd2-105">Especifica la categoría PnP-X a la que pertenece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="ddcd2-106">Se puede especificar más de una categoría.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="ddcd2-107">Uso</span><span class="sxs-lookup"><span data-stu-id="ddcd2-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="ddcd2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ddcd2-108">Attributes</span></span>

<span data-ttu-id="ddcd2-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ddcd2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ddcd2-110">Child elements</span></span>

<span data-ttu-id="ddcd2-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ddcd2-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ddcd2-112">Parent elements</span></span>



| <span data-ttu-id="ddcd2-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="ddcd2-113">Element</span></span>                                                   | <span data-ttu-id="ddcd2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddcd2-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddcd2-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="ddcd2-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="ddcd2-116">Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ddcd2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddcd2-117">Remarks</span></span>

<span data-ttu-id="ddcd2-118">Los dispositivos también pueden especificar una subcategoría de dispositivo para una categoría de dispositivo más descriptiva.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="ddcd2-119">Por ejemplo, "Phone. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica un dispositivo que es un dispositivo móvil de Microsoft Windows con una cámara y un reproductor de música.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="ddcd2-120">La categoría de dispositivo principal de este dispositivo sería "teléfonos".</span><span class="sxs-lookup"><span data-stu-id="ddcd2-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="ddcd2-121">Para especificar más de una categoría de dispositivo, separe las categorías con un espacio.</span><span class="sxs-lookup"><span data-stu-id="ddcd2-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="ddcd2-122">Por ejemplo, "almacenamiento de impresoras" identifica un dispositivo con una categoría principal de "impresoras" y una categoría secundaria de "almacenamiento".</span><span class="sxs-lookup"><span data-stu-id="ddcd2-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="ddcd2-123">Si hay un elemento **PnPXDeviceCategory** , al menos un elemento [**hospedado**](hosted.md) debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="ddcd2-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="ddcd2-124">Del mismo modo, si los elementos **PnPXHardwareId** y **PnPXCompatibleId** están presentes en un elemento **hospedado** , al menos un elemento **PnPXDeviceCategory** debe estar presente dentro del elemento [**thisModelMetadata**](thismodelmetadata.md) .</span><span class="sxs-lookup"><span data-stu-id="ddcd2-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="ddcd2-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ddcd2-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ddcd2-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddcd2-126">Minimum supported system</span></span><br/> | <span data-ttu-id="ddcd2-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddcd2-127">Windows Vista</span></span> |
| <span data-ttu-id="ddcd2-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ddcd2-128">Can be empty</span></span>                        | <span data-ttu-id="ddcd2-129">Sí</span><span class="sxs-lookup"><span data-stu-id="ddcd2-129">Yes</span></span>           |



 

 





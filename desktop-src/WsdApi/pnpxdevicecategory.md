---
description: Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996592"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="46f6c-104">PnPXDeviceCategory, elemento</span><span class="sxs-lookup"><span data-stu-id="46f6c-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="46f6c-105">Especifica la categoría PnP-X a la que pertenece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46f6c-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="46f6c-106">Se puede especificar más de una categoría.</span><span class="sxs-lookup"><span data-stu-id="46f6c-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="46f6c-107">Uso</span><span class="sxs-lookup"><span data-stu-id="46f6c-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="46f6c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46f6c-108">Attributes</span></span>

<span data-ttu-id="46f6c-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="46f6c-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="46f6c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46f6c-110">Child elements</span></span>

<span data-ttu-id="46f6c-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="46f6c-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="46f6c-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="46f6c-112">Parent elements</span></span>



| <span data-ttu-id="46f6c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="46f6c-113">Element</span></span>                                                   | <span data-ttu-id="46f6c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="46f6c-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f6c-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="46f6c-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="46f6c-116">Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="46f6c-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="46f6c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46f6c-117">Remarks</span></span>

<span data-ttu-id="46f6c-118">Los dispositivos también pueden especificar una subcategoría de dispositivo para una categoría de dispositivo más descriptiva.</span><span class="sxs-lookup"><span data-stu-id="46f6c-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="46f6c-119">Por ejemplo, "Phones.WindowsMobile Cameras.DigitalStcamera MediaDevices.MusicPlayer" identifica un dispositivo que es un dispositivo de Microsoft Windows Mobile con una cámara y un reproductor de música.</span><span class="sxs-lookup"><span data-stu-id="46f6c-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="46f6c-120">La categoría de dispositivo principal para este dispositivo sería "Teléfonos".</span><span class="sxs-lookup"><span data-stu-id="46f6c-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="46f6c-121">Para especificar más de una categoría de dispositivo, separe las categorías con un espacio.</span><span class="sxs-lookup"><span data-stu-id="46f6c-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="46f6c-122">Por ejemplo, "Almacenamiento de impresoras" identifica un dispositivo con una categoría principal de "Impresoras" y una categoría secundaria de "Almacenamiento".</span><span class="sxs-lookup"><span data-stu-id="46f6c-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="46f6c-123">Si hay **un elemento PnPXDeviceCategory** presente, al menos un elemento hospedado debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md)</span><span class="sxs-lookup"><span data-stu-id="46f6c-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="46f6c-124">Del mismo modo, si los elementos **PnPXHardwareId** y  **PnPXCompatibleId** están presentes en un elemento hospedado, debe haber al menos un elemento **PnPXDeviceCategory** dentro del elemento [**thisModelMetadata.**](thismodelmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="46f6c-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="46f6c-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="46f6c-125">Element information</span></span>



| <span data-ttu-id="46f6c-126">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="46f6c-126">Label</span></span> | <span data-ttu-id="46f6c-127">Value</span><span class="sxs-lookup"><span data-stu-id="46f6c-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="46f6c-128">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f6c-128">Minimum supported system</span></span><br/> | <span data-ttu-id="46f6c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46f6c-129">Windows Vista</span></span> |
| <span data-ttu-id="46f6c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46f6c-130">Can be empty</span></span>                        | <span data-ttu-id="46f6c-131">Sí</span><span class="sxs-lookup"><span data-stu-id="46f6c-131">Yes</span></span>           |



 

 





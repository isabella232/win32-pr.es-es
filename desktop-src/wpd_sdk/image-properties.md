---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de imagen.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propiedades de la imagen (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671783"
---
# <a name="image-properties"></a><span data-ttu-id="8bab9-103">Propiedades de la imagen</span><span class="sxs-lookup"><span data-stu-id="8bab9-103">Image Properties</span></span>

<span data-ttu-id="8bab9-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de imagen.</span><span class="sxs-lookup"><span data-stu-id="8bab9-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="8bab9-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8bab9-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="8bab9-106">VarType</span><span class="sxs-lookup"><span data-stu-id="8bab9-106">VarType</span></span>     | <span data-ttu-id="8bab9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bab9-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bab9-108">**\_BITDEPTH de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="8bab9-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-109">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-110">Profundidad de bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8bab9-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8bab9-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ \_ Estado corregido de color de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="8bab9-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-112">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-113">Una enumeración de [**\_ \_ \_ \_ valores de estado corregidos en color de WPD**](wpd-color-corrected-status-values.md) que especifica si el archivo se ha corregido por color. Esto impide que varios dispositivos corrijan automáticamente la imagen durante el procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="8bab9-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="8bab9-114">**\_ \_ Estado recortado de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="8bab9-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-115">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-116">Una enumeración de [**\_ \_ \_ valores recortados de WPD**](wpd-cropped-status-values.md) que especifica si el archivo se ha recortado. Esto impide que varios dispositivos recorten automáticamente la imagen durante el procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="8bab9-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="8bab9-117">**\_Índice de \_ exposición de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="8bab9-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-118">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-119">Valor que identifica la configuración de velocidad de la película cuando se capturó esta imagen. La configuración corresponde a las designaciones ISO de ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="8bab9-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="8bab9-120">Normalmente, un dispositivo admite valores enumerados discretos, pero es posible el control continuo sobre un intervalo.</span><span class="sxs-lookup"><span data-stu-id="8bab9-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="8bab9-121">Un valor de 0xFFFFFFFF corresponde a la configuración automática de ISO.</span><span class="sxs-lookup"><span data-stu-id="8bab9-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="8bab9-122">**tiempo de exposición de la imagen de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="8bab9-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-123">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-124">Identifica la velocidad del obturador del dispositivo cuando se capturó esta imagen. Las unidades están en segundos escaladas por 10000.</span><span class="sxs-lookup"><span data-stu-id="8bab9-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="8bab9-125">**\_FNUMBER de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="8bab9-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8bab9-126">**VT\_UI4**</span></span> | <span data-ttu-id="8bab9-127">Identifica el valor de abertura de la lente cuando se capturó esta imagen. Las unidades son iguales al número f escalado por 100.</span><span class="sxs-lookup"><span data-stu-id="8bab9-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="8bab9-128">**\_ \_ resolución horizontal de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="8bab9-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8bab9-129">**VT\_R8**</span></span>  | <span data-ttu-id="8bab9-130">Indica la resolución horizontal de una imagen, en puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="8bab9-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8bab9-131">**\_ \_ resolución vertical de imagen de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="8bab9-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="8bab9-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8bab9-132">**VT\_R8**</span></span>  | <span data-ttu-id="8bab9-133">Indica la resolución vertical de una imagen, en puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="8bab9-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8bab9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bab9-134">Requirements</span></span>



| <span data-ttu-id="8bab9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bab9-135">Requirement</span></span> | <span data-ttu-id="8bab9-136">Value</span><span class="sxs-lookup"><span data-stu-id="8bab9-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bab9-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bab9-137">Header</span></span><br/> | <dl> <span data-ttu-id="8bab9-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bab9-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bab9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bab9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bab9-140">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="8bab9-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




